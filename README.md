# BackTestingStockProject
Back Testing Stock Project 
Stock Backtesting Project: 5-Day Drop and 3% Recovery Strategy
Project Overview

This project backtests a stock trading strategy using historical U.S. stock market data from Yahoo Finance through the yfinance Python package. The goal of the project is to test whether buying stocks after a short-term price drop can produce stronger results than a simple Buy-and-Hold benchmark.

The strategy is tested across 20 randomly selected S&P 500 stocks from January 1, 2012 through December 31, 2025.

Strategy Summary

The strategy follows a simple rule-based approach:

Calculate each stock’s 5-day return using closing prices.
Buy when the stock drops 5% or more over the previous 5 trading days.
To avoid look-ahead bias, the buy signal is created after the close and the trade is executed on the next trading day.
Hold the position until the stock rises 3% or more from the entry price.
If the 3% profit target is not reached before the end of the backtest, the position is sold on the final trading day.
Selected Stocks

The project uses the following 20 stocks:

ANET, TMO, TMUS, QCOM, BA, VZ, TJX, SCHW, UNP, WELL, UBER, BX, CB, PLD, SPGI, COF, LMT, SYK, SBUX, FTNT

Tools and Libraries

This project was built using:

Python
pandas
numpy
yfinance
matplotlib
openpyxl
python-pptx, optional for PowerPoint creation
Performance Metrics

The backtest calculates the following metrics for each stock:

Final Strategy Value
Final Buy-and-Hold Value
Strategy Total Return
Buy-and-Hold Total Return
Strategy Annual Return
Buy-and-Hold Annual Return
Strategy Volatility
Buy-and-Hold Volatility
Strategy Sharpe Ratio
Buy-and-Hold Sharpe Ratio
Strategy Max Drawdown
Buy-and-Hold Max Drawdown
Number of Trades
Average Days Held
Winning Trades
Losing Trades
Win Rate
Project Outputs

The Python script creates:

A summary-only Excel file
backtesting_results_20_stocks_summary_only.xlsx
PowerPoint-ready PNG visuals in the folder
ppt_visuals_20_stocks
Optional PowerPoint file
stock_backtesting_summary_visuals_20_stocks.pptx
Visuals Created

The project creates the following visuals:

Strategy vs Buy-and-Hold Total Return
Final Portfolio Value Comparison
Strategy Max Drawdown by Ticker
Strategy Win Rate by Ticker
Average Days Held by Ticker
Strategy Risk vs Return Scatter Plot
Top 10 Stocks by Strategy Total Return Table
Key Takeaways

The backtest shows that the short-term drop strategy can generate positive returns for several stocks, but Buy-and-Hold often performs better over long time periods. The main reason is market exposure. A Buy-and-Hold strategy stays invested through long-term growth periods, while the drop strategy only enters after specific price declines.

The strategy also shows high win rates for many stocks because it waits for a 3% recovery before selling. However, high win rate alone does not mean the strategy is better. Max drawdown, average days held, and total return are important because they show how much risk and time the strategy takes to produce results.

Limitations

This project is for educational purposes only. It does not include transaction costs, taxes, slippage, bid-ask spreads, or real-time trading constraints. Results are based on historical data and should not be interpreted as financial advice.

How to Run

Install the required packages:

pip install yfinance pandas numpy matplotlib openpyxl python-pptx

Run the script:

python PythonStockBackTestingProject_20Stocks_SummaryVisuals.py

After the script runs, review the Excel summary file and the PNG visuals created for presentation use.

AI Disclosure

AI tools were used to help troubleshoot Python code, improve code structure. The final project logic, strategy interpretation, and analysis were reviewed and edited by the author.
