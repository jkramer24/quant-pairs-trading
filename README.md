# Correlated Coins: A Data-Driven Approach to Crypto Pairs Trading
**Jon Kramer**

## Introduction
This project evaluates three pairs trading strategies within the cryptocurrency market. All three strategies use historical data to find correlations between various coins as well as generate trading signals.

## Data Collection and Preprocessing
- Data from Yahoo Finance (daily closing prices for BTC and 25 other cryptos)
- Created synthetic basket of 25 coins vs. BTC
- Computed log returns and built a correlation matrix to identify strong pairs

## Optimization
- Chose pairs based on correlation matrix
- Built regression models for signal construction
- Optimized entry/exit thresholds for Sharpe ratio

---

## 📈 Strategy I: BTC & Basket of 25 Cryptocurrencies

**Signal:** Z-score of spread between BTC and synthetic basket  
**Entry/Exit Thresholds:** 3.0 / 0.5

**Performance:**  
Sharpe Ratio: **0.597**

> Demonstrated consistent mean-reversion and modest profits.

---

## 📉 Strategy II: BTC & STETH

**Signal:** Beta-weighted spread from linear regression  
**Entry/Exit Thresholds:** 3.0 / 0.5

**Performance:**  
Sharpe Ratio: **0.454**

> Captured some mean-reversion, but limited profitability due to weaker relationship.

---

## 🚀 Strategy III: ADA & XLM

**Signal:** Regression-weighted spread  
**Entry/Exit Thresholds:** 2.0 / -2.0

**Performance:**  
Sharpe Ratio: **1.543**

> Strongest performance. High correlation (0.81), but more consistent and profitable divergence patterns.

---

## Statistical Significance

OLS Regression of Strategy III vs. benchmark of top 25 cryptos:

- **Alpha:** 0.0008 (t = 1.828)
- **Beta:** 0.0705 (t = 5.297)
- **R-squared:** 0.081

> Low market sensitivity and statistically significant alpha. Strategy is largely market-neutral.

---

## Conclusion

This project showed that:
- BTC-based strategies were modest but consistent.
- A non-BTC pair (XLM & ADA) delivered much stronger returns.
- Pair selection and signal construction are crucial.
- Market-neutral strategies can be achieved through careful pair selection and regression modeling.

---
