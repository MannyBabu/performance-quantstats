# performance-quantstats
Quantstats library (https://github.com/ranaroussi/quantstats) is easy to use, quick way to build things like tearsheets
One issue I ran into has to to wth the latest version is this error:
"pandas version "Cannot compare tz-naive and tz-aware datetime-like objects" "
This is an issue with the way Quantstats works with yfinance (both by the same authos)
I downgraded to yfinance-0.1.74 instead of picking up the latest

alternately, you can remove the timezone from the timeseries 

Below is an example showing how to create a portfolio and plot it against a benchmark

port_dict = {'AAPL': 0.3, 'AMZN': 0.3, 'NVDA': 0.41469118072} 
benchmark_dict = {'SPY': 1.0}

port_index = qs.utils.make_index(port_dict)
benchmark_index = qs.utils.make_index(benchmark_dict)

qs.reports.basic(port_index, benchmark_index)

With just these lines, you should see a plot that shows how the desired portfolio compares to a benchmark. 
Of course, you can add starting value, period closes
