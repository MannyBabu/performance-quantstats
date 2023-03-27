# performance-quantstats
Quantstats library (https://github.com/ranaroussi/quantstats) is easy to use, quick way to build things like tearsheets
One issue I ran into has to to wth the latest version is this error:
"pandas version "Cannot compare tz-naive and tz-aware datetime-like objects""
This is an issue with the way Quantstats works with yfinance (both by the same authos)
I downgraded to yfinance-0.1.74 instead of picking up the latest
