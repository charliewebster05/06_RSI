# 06_RSI

RSI-Based Strategy for S&P 500 with Profit and Win Rate Evaluation

This project implements a Python-based pipeline that calculates the Relative Strength Index (RSI) for every stock in the S&P 500, and evaluates a basic trading strategy inspired by Algovibes.

# 📌 Strategy Overview
The strategy scans all S&P 500 tickers and generates buy signals when:

RSI < 30 → Stock is considered oversold.
Close price > 200-day moving average → Indicates long-term bullish trend.
These conditions aim to capture short-term reversals within strong upward trends.

# 🛠️ Key Components
RSI Calculation: Uses 14-period exponentially weighted averages to compute relative strength.
200-day Moving Average (MA200): Calculated for trend confirmation.
Buy Signal: Generated when both RSI and MA200 conditions are met.
Sell Signal: Exits are based on a future condition (e.g. RSI > 40 within the next 10 trading days).

# 💰 Profit and Win Rate Calculation
For each stock:

Buy is assumed the day after a signal is triggered.
Sell is simulated when the RSI crosses above 40 within the next 10 days.
Profit is calculated as:
(Sell Price - Buy Price) / Buy Price
Win rate is the ratio of trades with positive returns to total trades.
This gives a basic measure of the strategy's effectiveness across the index.

# 📊 Output
The script outputs:

A list of buy and sell dates for each ticker
Profit percentages per trade
Total win rate across all trades
Optional plots of signals and RSI values per ticker
