STOCK PRICE PREDICTION & TRADING STRATEGY USING XGBOOST AND TECHNICAL INDICATORS
-------------------------------------------------------------------------------

PROJECT DESCRIPTION
-------------------
This project uses the XGBoost machine learning algorithm to predict the next-day 
direction (up or down) of a stock's closing price based on multiple technical 
indicators. It then simulates a trading strategy based on these predictions.

The technical indicators include:
 - Simple Moving Average (SMA)
 - Exponential Moving Average (EMA)
 - Relative Strength Index (RSI)
 - Moving Average Convergence Divergence (MACD)
 - Bollinger Bands
 - Daily Volume Change (%)

The code downloads historical stock market data via Yahoo Finance, calculates 
these indicators, trains the XGBoost model, and then compares a Buy & Hold 
strategy to the model's predictive strategy.

FEATURES
--------
1. Automatic historical data download from Yahoo Finance.
2. Comprehensive technical indicator generation using the "ta" library.
3. XGBoost-based binary classification model to predict next-day price movement.
4. Strategy performance simulation and multiple graph visualizations:
   - Cumulative returns
   - Daily returns
   - Return distribution histograms
   - Rolling volatility

CURRENT STATUS
--------------
⚠️ IMPORTANT: The current model produces VERY POOR RESULTS in most cases.
During testing, the XGBoost-based strategy often underperforms the simple 
Buy & Hold approach and may even result in significant simulated losses.

This version:
 - Has no real predictive power on out-of-sample data.
 - Does not perform extensive hyperparameter tuning.
 - Ignores transaction costs, slippage, and realistic execution.
 - Uses a basic set of indicators without feature optimization.

These bad results are expected due to the difficulty of stock prediction with 
simplistic models and limited feature engineering.

INSTALLATION
------------
Requirements:
 - Python 3.x
 - Libraries: yfinance, pandas, numpy, ta, xgboost, matplotlib, scikit-learn

You can install dependencies with:
    pip install yfinance pandas numpy ta xgboost matplotlib scikit-learn

USAGE
-----
1. Adjust ticker symbol, date range, or indicators in the script as needed.
2. Run the script:
       python main.py
3. View model performance metrics printed in the terminal.
4. Examine the generated plots for strategy comparison.

INTERPRETING RESULTS
--------------------
 - Expect the model’s predictions and trading strategy to perform poorly.
 - Cumulative Returns: Will likely be worse than Buy & Hold.
 - Daily Returns: May show high variability and frequent losses.
 - Histograms: Likely to have a higher frequency of negative returns.
 - Rolling Volatility: May indicate unstable performance.

FUTURE IMPROVEMENTS
-------------------
 - Add hyperparameter optimization (GridSearchCV, Optuna).
 - Include more advanced indicators like ATR, Stochastic Oscillator, OBV.
 - Implement walk-forward optimization and rolling retraining.
 - Factor in transaction costs and realistic order execution.
 - Develop a parameterized strategy for multiple tickers.
 - Integrate with backtesting frameworks like Backtrader.
 - Consider ensemble models or deep learning approaches.
 - Apply proper feature selection and engineering to reduce noise.

DISCLAIMER
----------
This project is for educational and research purposes only.
It is NOT financial advice. Trading in financial markets carries risk, 
and past performance — especially poor performance in this case — 
is NOT indicative of future results.

