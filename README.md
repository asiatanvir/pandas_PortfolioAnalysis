# PORTFOLIO ANALYSIS

#### Background

You have been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

You just learned these quantitative analysis techniques with Python and Pandas, and you want to determine which portfolio is performing the best across multiple areas: volatility, returns, risk, and Sharpe ratios.

#### What You’re Creating
You need to create a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. You will be given the historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. You will then use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500 IndexLinks to an external site.).


#### Instructions
The instructions for this assignment are divided into three parts:

1. Prepare the Data

2. Perform Quantitative Analysis

3. Create a Custom Portfolio

### Prepare the Data
First, you will read in and clean several CSV files for analysis. The CSV files contain data on whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Use the Whale Analysis starter code to complete the following steps:

1  Use Pandas to read the following CSV files into DataFrames. Be sure to convert the dates to a DateTimeIndex.

     whale_returns.csv: Contains returns of some famous "whale" investors' portfolios.

     algo_returns.csv: Contains returns from the in-house trading algorithms from your company.

     sp500_history.csv: Contains historical closing prices of the S&P 500 Index.

2  Identify and remove null values.

3  Remove any non-numeric values (e.g., dollar signs) from the DataFrames and convert the data types as needed.

4  The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. Convert the S&P 500 closing prices to daily returns.

5  Join Whale Returns, Algorithmic Returns, and the S&P 500 Returns into a single DataFrame with columns for each portfolio's returns.

returns-dataframe.png

### Perform Quantitative Analysis
Analyze the data to determine if any of the portfolios outperform the stock market (that is, the S&P 500). Specifically, you will do a performance analysis and a risk analysis, and then calculate rolling statistics and Sharpe ratios.

#### Performance Analysis
1  Calculate and plot daily returns of all portfolios.

2  Calculate and plot cumulative returns for all portfolios. Does any portfolio outperform the S&P 500?

#### Risk Analysis
1  Create a box plot for each of the returns.

2  Calculate the standard deviation for each portfolio.

3  Determine which portfolios are riskier than the S&P 500.

4  Calculate the annualized standard deviation.

#### Rolling Statistics
1  Calculate and plot the rolling standard deviation for all portfolios, using a 21-day window.

2  Calculate and plot the correlation between each stock to determine which portfolios mimic the S&P 500.

3  Choose one portfolio, then calculate and plot the 60-day rolling beta between that portfolio and the S&P 500.

#### Rolling Statistics Challenge: Exponentially Weighted Average
An alternative method to calculate a rolling window is to find the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations. Try calculating the ewmLinks to an external site. with a 21-day half-life.

#### Sharpe Ratios
Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right? Follow these steps:

1  Using the daily returns, calculate the Sharpe ratios and visualize them in a bar plot.

2  Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.

### Create a Custom Portfolio
You’re excited that you were able to prove that the algorithmic trading portfolios are doing so well compared to the market and whales portfolios. However, now you are wondering whether you can choose your own portfolio that performs just as well as the algorithmic portfolios. Investigate by doing the following:

1  Use Google SheetsLinks to an external site. and its built-in GOOGLEFINANCE function to choose 3–5 stocks for your portfolio.

2  Download the data as CSV files and calculate the portfolio returns.

3  Calculate the weighted returns for your portfolio, assuming equal number of shares per stock.

4  Add your portfolio returns to the DataFrame with the other portfolios.

5  Run the following analyses:

    Calculate the annualized standard deviation.
    Calculate and plot the rolling standard deviation with a 21-day window.
    Calculate and plot the correlation.
    Calculate and plot beta for your portfolio compared to the S&P 60 TSX.
    Calculate the Sharpe ratios and generate a bar plot.

How does your portfolio perform?