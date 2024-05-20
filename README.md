# Portfolio Optimization using Efficient Frontier and Sharpe Ratio

# Introduction
This project aims to develop an optimization model that allocates investments across a portfolio that maximizes return and minimizes risk.

This return-risk tradeoff is done using Mean-Variance Optimization (MVO).
MVO focuses on creating a portfolio that maximizes return (Mean) when risk is given and minimizes risk (Variance or Standard Deviation) when return is given.

We later plot a curve representing a set of optimal portfolios, offering the highest expected return for a given level of risk.

We then use the Sharpe Ratio to calculate the return on an investment compared to its risk.
The formula is as follows:

$$ Sharpe Ratio = \frac{{R_p} - {R_f}}{{\sigma_p}} $$

where

Rp - the average return of the portfolio or investment

Rf - risk-free rate of return (return of an investment over some time with zero risk

sigma - standard deviation of the portfolio or investment

# Data Collection
Fetches historical stock prices from Quandl.

# Data Preprocessing
Checks for null values and calculates returns as the percentage change in stock value.

# Expected Returns and Covariance Matrix
The expected return is the mean of the probability distribution of possible returns of an asset.
Simply put, it is the average return an investor might expect over a given time period.

For a series of historical returns, Ri

$$ E(R) = (1/n)*\sum_{i=1}^n {R_i} $$

where

n - number of periods

Annually,

$$ E({R_a}) = E({R_d}) * 252 $$

(assuming there are 252 trading days per year)
and a - annual, and d - daily

The Covariance matrix captures the relation between pairs of assets in a portfolio.

It is used to understand the risk and diversification benefits of owning different assets together.

Also, for assessing overall portfolio risk and optimizing the portfolio to achieve the best return-risk tradeoff (Mean-Variance optimization).

For any two assets **X** and **Y**:

$$ Cov(X,Y) = \frac{1}{n-1}*\sum_{i=1}^n ({X_i} - \bar{X}) * ({Y_i} - \bar{Y}) $$

Annually,

$$ \sum_{annual} = \sum_{daily} * 252 $$

# Optimization Problem
This step aims to find the optimal weights for the quadratic equation that minimize risk when return is given and maximize return when risk is given.

# Portfolio Performance Evaluation
Evaluate the performance of return cumulatively.

# Visualize the Efficient Frontier
The efficient frontier represents a set of optimal portfolios that give the highest return for a given level of risk and the lowest risk for a given level of expected return.
These portfolios are 'efficient' because they're well-balanced (Mean-Variance Optimization, i.e., Return-risk tradeoff).

# Sharpe Ratio
To estimate the optimized portfolio, we calculate the Sharpe Ratio.
The higher the Sharpe Ratio, the better the return-to-risk ratio.
It is an indication that it is safer to invest in that particular stock.
