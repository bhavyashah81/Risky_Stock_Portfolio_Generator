# Risky Stock Portfolio Generator
A financial analysis system that creates high-risk investment portfolios by identifying volatile stocks and maximizing sector correlations.

## Features
**Risk Maximization**: Identifies highest volatility stocks using standard deviation metrics
**Sector Analysis**: Groups and analyzes stocks across 10+ industry sectors
**Correlation Optimization**: Maximizes positive correlations between holdings
**Smart Filtering**: Filters stocks by volume (>10,000 daily avg) and data availability
**Concentration Strategy**: Allocates 60% of capital to top 2 correlated stocks

## Technologies and Languages Used
**Languages**: Python, Jupyter Notebook
**Libraries**: pandas, numpy, yfinance, matplotlib, numpy-financial, IPython
**APIs**: Yahoo Finance API
**Tools**: Git, CSV processing

## Usage

### Running the Portfolio Generator

```bash
python3 "final Finance Project.py"
```

### Input Format
The script reads `Sample Tickers.csv` containing stock symbols:
```
Tickers
IRBT
ENFAU
UVE
OPOF
```

### Generating a Portfolio
To generate a risky portfolio from stock tickers:

```bash
python3 "final Finance Project.py"
```

This will:
1. Load stock tickers from Sample Tickers.csv
2. Fetch historical data using yfinance (2019-2021)
3. Calculate volatility for each stock
4. Group stocks by sectors
5. Identify highest-risk sector
6. Calculate sector correlations
7. Select top 10 stocks based on risk metrics
8. Output portfolio to Stocks_Group_16.csv

## Algorithm Details
**Risk Metric**: Standard deviation of monthly returns
**Time Period**: 2019-01-01 to 2021-11-30
**Portfolio Size**: 10 stocks
**Capital Allocation**: $100,000 total
**Top Stock Weight**: 35% (highest volatility)
**Second Stock Weight**: 25% (highest correlation)
**Remaining Stocks**: 5% each ($5,000 minimum)

## Output Format
The generated CSV contains:

Ticker: Stock symbol
Shares: Number of shares to purchase
Weight: Portfolio allocation percentage

Example output:
```
,Ticker,Shares
1,APA,1372.195
2,FANG,263.030
3,ECL,22.558
4,NEM,102.476
5,APD,18.438
```

## Dependencies
Install required packages:

```bash
pip3 install pandas numpy numpy-financial yfinance matplotlib jupyter notebook ipykernel
```

Required packages:

pandas >= 1.3.0
numpy >= 1.21.0
numpy-financial >= 1.0.0
yfinance >= 0.1.70
matplotlib >= 3.4.0
jupyter >= 1.0.0
notebook >= 6.4.0
ipykernel >= 6.0.0