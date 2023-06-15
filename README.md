# Algorithmic-Trading-Strategy
This repository contains a Python code for fetching US stock data using the Alpha Vantage API and implementing a simple trading strategy based on technical indicators.

## Requirements:
  - Python 3.x
  - pandas
  - matplotlib
  - mplfinance

## Class and Methods
### ScriptData
- fetch_intraday_data(script): Fetches intraday data for the specified stock script using the Alpha Vantage API.
- convert_intraday_data(script): Converts the fetched intraday data into a pandas DataFrame.
- __getitem__(key): Retrieves the data for a specific stock script.
- __contains__(key): Checks if the data for a specific stock script is available.

### Strategy
- get_script_data(): Fetches intraday data for the specified stock and computes the indicator data.
- compute_indicator_data(timeperiod): Converts the intraday data into a pandas DataFrame and calculates the indicator data.
- get_signals(): Generates trading signals based on the computed indicators.
- plot_candlestick_chart(): Plots a candlestick chart for the fetched intraday data.

## Usage
1. Install the required libraries using the following command:
```
pip install pandas matplotlib mplfinance
```
2. Use the get_script_data() method of the Strategy class to fetch intraday data for a specific stock and compute the indicator data:
```
strategy = Strategy('AAPL')
strategy.get_script_data()
```
3. Use the get_signals() method to generate trading signals based on the computed indicators:
```
strategy.get_signals()
```
4. Plot a candlestick chart for the fetched data using the plot_candlestick_chart() method:
```
strategy.plot_candlestick_chart()
```
