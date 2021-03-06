# ystockQuery
A Yahoo Finance wrapper for stock quotes and historical data

Install:

```
pip install ystockQuery
```

Examples:

```
import ystockQuery

# init Ystock class for Square, Inc.
sq = ystockQuery.Ystock("SQ")

# return a list of history data between start date and end date
hist = sq.history("1-1-2019", "1-1-2020")

# return data for a specifc date from the history
data = hist.atDate("3-12-2019")
print(data.getVolume())
print(data.getLow())
print(data.getOpen())
print(data.getHigh())
print(data.getClose())
print(data.getAdjClose())

# format full history data to dict format
print(hist.toDict())
"""
{
  1546439400: 
  {
    'volume': 5273100,
    'low': 36.0,
    'open': 36.20000076293945,
    'high': 36.75,
    'close': 36.52000045776367,
    'adjclose': 34.28937911987305
  }
}
"""
```

Requirements

See ``requirements.txt``
