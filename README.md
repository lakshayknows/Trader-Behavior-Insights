# Trader Behavior Analysis Under Market Sentiment  
```markdown
Bitcoin Fear–Greed Index × Hyperliquid Trading Data

## Project Overview

This project analyzes the relationship between Bitcoin market sentiment and trader behavior using historical trading data merged with the Bitcoin Fear–Greed Index. The goal is to understand how sentiment regimes (Fear vs Greed) influence risk-taking behavior, trading activity, and performance dispersion across traders.

The analysis focuses on behavioral dynamics rather than price prediction, with particular emphasis on how market sentiment amplifies existing trader skill and biases.

---

## Datasets Used

1. Bitcoin Fear–Greed Index  
   - Fields: Date, Index Value, Sentiment Classification  
   - Represents daily market psychology (Fear / Greed)

2. Hyperliquid Historical Trader Data  
   - Fields include: Account, Coin, Trade Size (USD), Execution Price, Side, Closed PnL, Timestamp, etc.  
   - Analysis is restricted to Bitcoin trades only

---

## Key Questions Explored

- Do traders take on more risk during Greed periods?
- How does sentiment impact trading activity and profitability?
- Are top-performing traders resilient to sentiment changes?
- Does Greed disproportionately harm lower-performing traders?

---

## Methodology

### Data Preparation
- Converted all timestamps to datetime format
- Filtered for Bitcoin trades only
- Retained only closed trades with valid Closed PnL
- Cleaned and aligned both datasets on a daily time basis

### Feature Engineering
- Daily trade counts
- Average trade size (USD) as a proxy for risk-taking
- Aggregate daily Closed PnL
- Trader-level total PnL
- Skill-based segmentation (Top 20% vs Bottom 20% traders)

### Exploratory Data Analysis
- Time-series analysis of market sentiment
- Trading activity comparison across sentiment regimes
- PnL distribution analysis under Fear vs Greed
- Risk–reward analysis using trade size vs PnL
- Performance comparison between skilled and unskilled traders
- Dual-axis analysis of sentiment and aggregate profitability

---

## Key Findings

- Traders exhibit higher risk-taking during Greed periods, with average trade size increasing to approximately $27,000 compared to approximately $20,000 during Fear periods.
- Market sentiment amplifies performance differences:
  - Top 20% traders remain consistently profitable across both Fear and Greed regimes.
  - Bottom 20% traders perform modestly during Fear but incur losses during Greed.
- Greed regimes show wider PnL dispersion and higher downside risk, indicating overconfidence-driven behavior.
- Larger trade sizes do not consistently translate into higher profitability, especially during Greed periods.

---

## Insights and Next Steps

- Market sentiment functions primarily as a behavioral amplifier rather than a direct profitability signal.
- Sentiment-aware risk management, such as dynamic position sizing or leverage constraints, could help reduce drawdowns during Greed regimes.
- Future extensions may include behavioral clustering of traders and sentiment-conditioned risk frameworks to identify resilient trading strategies.

---

## Tools and Technologies

- Python  
- pandas, numpy  
- matplotlib  
- Jupyter Notebook  

---

## Project Structure

```
```
Trader-Behavior-Sentiment-Analysis/
│
├── trader_behavior_sentiment_analysis.ipynb
└── README.md

```

---

## How to Run

1. Clone the repository  
2. Open the notebook  
   jupyter notebook trader_behavior_sentiment_analysis.ipynb  

---

This project was completed as part of a pre-internship assignment for Primetrade.ai.
```
