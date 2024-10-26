# Investment Portfolio Optimization and Risk Allocation Analysis

## Project Overview 
### Objective
This project provides a hands-on approach to optimizing a portfolio of stocks, exchange-traded funds (ETFs), and foreign exchange (FX) spot rates, based on various financial metrics. The aim is to help investors and analysts maximize returns while managing risks effectively, using different optimization strategies. The user inputs tickers (up to 50), and the project pulls relevant financial data to generate actionable insights, including visualizations of asset allocations and portfolio performance. This process is further enhanced by historical backtesting and correlation analysis.

### Data Collection
The historical price data of the selected tickers is collected from Yahoo! Finance for a specified four-year time frame, from 2020-01-01 to 2024-01-01. This data includes daily stock prices, ETFs, and FX spot rates, which are then processed to compute daily returns. The code supports multiple types of tickers, including:

- Stocks (e.g., AAPL, AMZN)
- ETFs (e.g., VOO, SPY)
- FX Spot Rates (e.g., JPY=X for Japanese Yen)

### Financial Models
The project utilizes several optimization techniques, including:

- Sharpe Ratio: Maximizes return per unit of risk by considering the excess return

- Kelly Criterion: Determines the optimal proportion of the portfolio to invest in each asset, aiming to maximize the expected logarithm of wealth

- Conditional Value at Risk (CVaR): Minimizes potential losses in adverse scenarios, enhancing overall risk management

- Risk Parity: Balances risk across the portfolio to ensure equal contributions to total risk from each asset

### Backtesting Performance
To assess the effectiveness of these models, the portfolio is backtested using an initial budget of $100,000. The backtesting process evaluates how each optimized portfolio would have performed over time. This includes:

- Plotting Cumulative Returns: The value of the portfolio is tracked from the start to the end of the test period

- Comparison of Models: The portfolio's growth under different optimization strategies (Sharpe Ratio, Kelly, CVaR, Risk Parity) is visualized to identify which model yields the best results

### Efficient Frontier Visualization
The Efficient Frontier represents the set of optimal portfolios offering the highest expected return for a defined level of risk. The visualization uses the mean-variance optimization framework and includes:

- Volatility vs. Return: Portfolios are plotted on a scatter plot with expected return on the y-axis and portfolio volatility (standard deviation) on the x-axis

- Sharpe Ratio Visualization: The efficient frontier is colour-coded to highlight portfolios based on their Sharpe Ratios. Higher Sharpe Ratios are shown in brighter colours

- Optimal Portfolio Markers: A star marks the most optimal portfolio based on the highest Sharpe Ratio.
An 'X' indicates other portfolios with lower risk at various volatility levels

### Correlation Heatmap:
In addition to portfolio optimization, the code generates a heatmap based on the correlation matrix of the returns. This helps investors understand how the selected assets move concerning one another. The correlation matrix reveals the degree to which asset prices are correlated:

- Correlation Coefficients: Values close to 1 indicate a strong positive correlation, while values close to -1 indicate a strong negative correlation. A value of 0 implies no correlation

- Interpretation: Highly correlated assets tend to move together, while uncorrelated or negatively correlated assets provide diversification benefits. The heatmap visually represents these relationships, aiding in the diversification strategy

#### Asset Allocation by Industry:
To provide a broader understanding of the portfolio's composition, the code generates a pie chart showing asset allocation by industry. This feature utilizes Yahoo! Finance's industry classifications to break down the investments by sectors

## Libraries and APIs
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `scipy`
- `yfinance`

## Relevant Resources and Articles
- https://www.daytrading.com/portfolio-optimization-techniques
- https://www.investopedia.com/articles/trading/04/091504.asp
- https://www.investopedia.com/articles/trading/04/091504.asp
- https://www.investopedia.com/terms/s/sharperatio.asp
- https://www.schwab.com/learn/story/calculate-sharpe-ratio-to-gauge-risk
- https://www.columbia.edu/~mh2078/FoundationsFE/MeanVariance-CAPM.pdf
- https://www.investopedia.com/terms/m/meanvariance-analysis.asp
- https://www.investopedia.com/terms/r/risk-parity.asp
- https://www.cmegroup.com/education/files/understanding-risk-parity-2013-06.pdf
