# Deep Reinforcement Learning for Portfolio Optimization

1. Introduction
   
   a) This Project deals with Portfolio Optimization for Stock Data using Reinforcement Learning.
   
   b) We used a model-free, value-based method for portfolio optimization because it does not require explicit modeling of market dynamics, making it suitable for environments with high uncertainty and non-stationary data.

   The value-based approach directly optimizes the portfolio's cumulative returns, balancing reward accumulation over time.

2. Reinforcement Model used: REINFORCE
   
   a) Framework 

    Agent: Neural network that learns optimal portfolio weight allocation across 10
            stocks.

    Environment: Custom PortfolioEnv class implementing market environment.
   
    State: Historical market data including price, returns, volatility, and technical
             indicators.
   
    Actions: Continuous portfolio weight allocation between 0 and 1 for each asset.
   
    Reward: Risk-adjusted returns considering transaction costs.
   
    Policy: Stochastic policy implemented via neural network generating portfolio
             weights.
   
   b) Dataset
   
      We have used the top 10 S&P 500 companies by market cap from 2005–2024: AAPL,
      MSFT, NVDA, AMZN, GOOG, GOOGL, META, TSLA, AVGO, WMT.

     Features include: Close, Daily Return, Volatility, MA 10, MA 50, RSI, Beta, Sharpe

     Ratio, Dividend Yield, Max Drawdown
   
     Train dataset: 2005–2020
     Test dataset: 2020–2024
   
4. Traditional Model Used: Mean-variance optimization (MVO)

   a) Dataset:

      The dataset comprises historical stock price data for the top 10 SP 500
      companies by market capitalization.

      Historical data spans the last 5 years, retrieved using yfinance.

5. Evaluation Parameters
   
   a) Sharpe Ratio (SR): Evaluates the ratio of average return to volatility.

   b) Maximum Drawdown (MDD): Measures stability during market downturns.

6. Results

   a) REINFORCE outperforms Traditional method MVO demonstrating strong performance

   b) Performance Analysis

   ![image](https://github.com/user-attachments/assets/72baa1ad-7d71-403f-a2fc-da525a70bb03)











