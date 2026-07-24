# Advanced Analytics & Statistical Modeling — Superstore Dataset

Task 4 of a data analytics project series: applying statistical analysis, time series
analysis, customer segmentation, and predictive modeling to the Superstore sales dataset.

## Overview

This project analyzes ~10,000 orders (2015–2018) from a retail superstore to answer
business questions around profitability, seasonality, and customer value, and to build a
model that flags orders likely to result in a loss.

## Contents

1. **Descriptive Statistics** — mean, median, mode, std dev, skewness for sales, profit,
   discount, quantity, and profit margin.
2. **Hypothesis Testing**
   - T-test: does discounting affect profit?
   - Chi-square test: is loss rate independent of region?
   - 95% confidence interval for mean profit margin.
3. **Time Series Analysis** — monthly sales trend, additive decomposition
   (trend/seasonality/residual), 3-month moving average forecast.
4. **Customer Segmentation** — RFM-style features, K-Means clustering (elbow method for
   optimal K), PCA 2D visualization, segment profiles with recommendations.
5. **Predictive Model** — logistic regression predicting whether an order is a loss
   (`is_loss`), evaluated on accuracy/precision/recall/F1, with top feature drivers.

## Key Findings

- Discounted orders average a **loss** (-$6.66), non-discounted orders average **$66.90**
  profit (t-test, p < 0.001).
- Loss rate varies significantly by region (chi-square, p < 0.001) — Central highest,
  West lowest.
- True mean profit margin: **11.1%–12.9%** (95% CI).
- Sales trend upward over 2015–2018 with strong Q4 (Sep/Nov/Dec) seasonality.
- Four customer segments identified: VIP, discount-driven/unprofitable, steady mid-tier,
  at-risk/lapsed.
- Logistic regression predicts loss-making orders with **94.3% accuracy** (96.4%
  precision, 72.2% recall). Discount level is the strongest driver.

## Repo Structure

```
.
├── Task4_Advanced_Analytics.ipynb   # Main analysis notebook (fully executed, outputs included)
├── data/
│   └── superstore_clean.csv         # Cleaned dataset used in the analysis
└── README.md

```

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook Task4_Advanced_Analytics.ipynb
```

## Tools Used

Python, pandas, NumPy, SciPy, scikit-learn, matplotlib, seaborn
