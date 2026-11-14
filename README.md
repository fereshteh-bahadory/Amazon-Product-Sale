# Amazon Sales Analysis

> **Status: in progress.** The exploratory analysis and customer segmentation are done; a predictive model and a KPI dashboard are planned (see the roadmap).

Exploratory business analysis of Amazon order data (3,203 orders from western US states) in Python.
The goal is to turn raw order data into answers a business can act on.

## Questions
1. How do sales, profit, and order volume evolve over time? How fast are orders shipped?
2. Which product categories drive sales, and which are actually profitable (margin, unit price)?
3. Where do orders come from?
4. Who are the most valuable customers, and what customer segments exist?

## Key findings
<!-- Fill in after running the notebook on the real data: one sentence with a number each. -->
- **Trend:** TODO
- **Categories:** TODO
- **Geography:** TODO
- **Customers:** TODO

## Methods
- Data cleaning and feature engineering with **pandas** (dates, location split, margin, unit price).
- Time-series aggregation and visualization with **matplotlib** and **seaborn**.
- Category and geographic analysis (sales and margin by state).
- **RFM analysis** (recency, frequency, monetary) with quintile scores and rule-based segments.
- **K-Means clustering** on log-scaled and standardized RFM features, with the number of clusters chosen by silhouette score.

## Dataset
[Amazon Sales Dataset on Kaggle](https://www.kaggle.com/datasets/anandshaw2001/amazon-sales-dataset).
Download `Amazon.csv` and put it in a `data/` folder (not included in this repository).

## How to run
```bash
pip install -r requirements.txt
mkdir data            # then place Amazon.csv inside it
jupyter notebook amazon_analysis.ipynb
```

## Repository structure
```
Amazon-Product-Sale/
├── amazon_analysis.ipynb
├── requirements.txt
├── README.md
└── data/            # Amazon.csv goes here (not tracked)
```

## Limitations
- Small, single-source dataset; the analysis is descriptive, not causal.
- No discount, cost, or competitor data, so no real price-elasticity or promotion analysis.

## Roadmap
- [ ] Predictive model for profit or sales per order (train/test split, evaluation metrics)
- [ ] KPI dashboard (Looker Studio or Power BI)
- [ ] Retention / CLTV modelling if longer history is available

## Author
Fereshteh Bahadorykhalily · [LinkedIn](https://www.linkedin.com/in/fereshte-bahadorykhalily-61591295/) · [GitHub](https://github.com/fereshteh-bahadory)
