# Portfolio Optimization and Risk Management using Rolling Backtests on NIFTY 50
# Overview
This project explores how different equity portfolio strategies perform in real market conditions using historical NIFTY 50 data from 2009 to 2022. Instead of relying only on simple benchmark investing, the study focuses on optimized portfolios and evaluates both returns and risk through a realistic rolling-window backtesting framework.

# What This Project Does
Builds multiple equity portfolios using quantitative finance concepts
Tests them out-of-sample using rolling formation and holding periods
Compares optimized strategies with the NIFTY 50 benchmark
Examines downside risk using Value-at-Risk (VaR)

# Data Used
Daily closing prices of NIFTY 50 constituent stocks
Market factor and risk-free rate data
Time period: January 2009 to December 2022
Stocks with incomplete data were removed, leaving a final universe of 45 stocks
Daily simple returns were used throughout the analysis

# Methodology

Portfolios were rebuilt every quarter using a 6-month formation window to estimate parameters such as returns, covariance, alpha, and beta.
The resulting weights were then held fixed for the next 3 months, generating out-of-sample returns.
This rolling process was repeated across 54 windows, helping avoid look-ahead bias and better reflect real-world investing.

# Portfolio Strategies
Global Minimum Variance (GMV): Focuses on minimizing portfolio risk
Mean–Variance (Tangency): Aims to maximize risk-adjusted returns
Equal-Weighted (EW): Allocates equal capital across all stocks
Active Portfolio: Selects stocks with statistically significant CAPM alpha

# Performance Evaluation
Portfolio performance was evaluated using:
Cumulative returns
Annualized mean returns and volatility
Sharpe Ratio
Information Ratio (relative to NIFTY 50)

# Key Findings
Optimized portfolios (GMV and Mean–Variance) clearly outperformed the NIFTY 50 over the long run
GMV delivered strong returns while maintaining lower volatility
The Active strategy showed little improvement over simple equal weighting, suggesting weak alpha persistence

# Risk Analysis (Value-at-Risk)
To study downside risk, a 99% Historical VaR was estimated for each holding period and compared with realized returns.
The results showed that historical VaR often underestimated risk, especially during high-volatility periods such as the COVID-19 market crash, highlighting limitations of static risk models.

# Tools & Libraries
Python
NumPy
Pandas
SciPy
Statsmodels
Matplotlib
Seaborn

