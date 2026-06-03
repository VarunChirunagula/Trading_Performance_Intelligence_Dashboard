# Trading Performance Intelligence Dashboard

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed Index) and trader performance on Hyperliquid. The objective is to understand how different market sentiment regimes influence trader profitability, trading behavior, risk-taking, and activity levels.

The analysis combines Bitcoin Fear & Greed sentiment data with historical Hyperliquid trading records to uncover actionable insights and potential trading strategies.

---

## Objective

To investigate:

* How trader profitability varies across Fear and Greed market conditions.
* Whether trader behavior changes based on market sentiment.
* Differences between frequent and infrequent traders.
* Long vs Short trading preferences under different sentiment regimes.
* Actionable trading strategies derived from observed patterns.

---

## Datasets

### 1. Bitcoin Fear & Greed Index

**Columns Used**

* Date
* Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)

Purpose:

* Represents overall market sentiment for each day.

### 2. Hyperliquid Historical Trader Data

**Columns Used**

* Account
* Trade ID
* Coin
* Side
* Direction
* Execution Price
* Size USD
* Closed PnL
* Timestamp

Purpose:

* Provides trader-level transaction and profitability information.

---

## Data Preparation

### Data Cleaning

* Removed duplicate records.
* Checked for missing values.
* Standardized date formats.
* Converted timestamps to daily granularity.

### Data Integration

* Merged trading data with Fear & Greed sentiment data using the trade date.
* Assigned a sentiment classification to every trade.

### Feature Engineering

Created the following analytical features:

| Feature            | Description                                  |
| ------------------ | -------------------------------------------- |
| Win Flag           | Indicates whether a trade was profitable     |
| Trade Count        | Total trades executed by each trader         |
| Trader Segment     | Frequent or Infrequent trader classification |
| Daily PnL          | Total daily profit/loss per trader           |
| Average Trade Size | Mean trade size in USD                       |
| Trade Frequency    | Number of trades executed per day            |

---

## Dashboard Components

### KPI Cards

* Total Traders
* Total Trades
* Total PnL
* Average Win Rate
* Average Trade Size

### Visualizations

1. Average PnL by Sentiment
2. Win Rate by Sentiment
3. Average Trade Size by Sentiment
4. Number of Trades by Sentiment
5. Long vs Short Ratio by Sentiment
6. Frequent vs Infrequent Trader Comparison

---

## Key Findings

### 1. Extreme Greed Produces Highest Profitability

Traders achieved their highest average profit during Extreme Greed periods, suggesting that bullish market conditions provide favorable trading opportunities.

### 2. Fear Leads to Larger Position Sizes

Average trade size was highest during Fear periods, indicating that traders tend to take larger positions when markets are under pressure.

### 3. Win Rates Improve During Extreme Greed

Trade success rates increased significantly during Extreme Greed conditions, highlighting the advantage of trading alongside strong market momentum.

### 4. Infrequent Traders Outperform Frequent Traders

Infrequent traders generated higher average profits than frequent traders, suggesting that selective trading may be more effective than excessive trading activity.

---

## Strategy Recommendations

### Recommendation 1: Increase Exposure During Extreme Greed

* Focus on momentum-based trading strategies.
* Allow larger profit targets during strong bullish sentiment.
* Prioritize trend-following setups.

### Recommendation 2: Apply Risk Controls During Fear

* Reduce position sizing.
* Use stricter stop-loss rules.
* Avoid emotional overexposure during market downturns.

---

## Tools Used

* Python

  * Pandas
  * NumPy

* Tableau Public

* Jupyter Notebook

---



## Conclusion

This analysis demonstrates a clear relationship between market sentiment and trader behavior. Extreme Greed periods are associated with higher profitability and win rates, while Fear periods encourage larger position sizes and increased risk-taking. These findings can be used to design sentiment-aware trading strategies and improve risk management decisions.
