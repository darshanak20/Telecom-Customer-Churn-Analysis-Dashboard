# Telecom Customer Churn Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Overview

A full-cycle data analytics project analysing customer churn for a 
telecom company. Starting from raw data exploration in Python through 
to a 5-page interactive Power BI dashboard, this project identifies 
why customers leave, when they are most at risk, and which active 
customers the retention team should prioritise calling.

**Business question:** *"Why are customers churning, and who do we 
contact today to stop it?"*

---

## Key Findings

| Driver | Churn Rate | Insight |
|---|---|---|
| Month-to-month contract | 50.8% | 4× higher than 2-year contracts |
| Fiber optic service | 40.9% | Highest among internet types |
| Electronic check payment | 43.1% | Billing friction = higher churn |
| High charge tier (>$65/mo) | 40.6% | Highest-paying = highest risk |
| 0 add-on services | ~42% | More services = more retention |

---

## Dashboard Pages

| Page | Title | Purpose |
|---|---|---|
| 1 | Executive Overview | Headline KPIs — churn rate, revenue lost, at-risk count |
| 2 | Churn Drivers | Why customers churn — contract, service, payment, charges |
| 3 | Customer Lifecycle | When customers churn — tenure trends, scatter analysis |
| 4 | At-Risk Tracker | Who to call — filterable list of 182 high-risk customers |
| 5 | Recommendations | 3 business actions with projected impact |

---

## Business Recommendations

**R1 — Target month-to-month customers at month 3–6**
Offer a discounted annual plan during the highest-risk window.
A 10% reduction in this segment saves ~$8,000/month.

**R2 — Nudge electronic check users to auto-pay**
Auto-pay customers churn at 17% vs 43% for electronic check.
A simple billing prompt could recover a significant share of 
at-risk revenue.

**R3 — Investigate fiber optic service quality**
Fiber customers churn at 41% — nearly 3× DSL. Survey churned 
fiber customers to determine if pricing or service quality 
is the root cause.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, feature engineering, EDA |
| Power BI | Dashboard, DAX measures, interactive visuals |
| Jupyter Notebook | Exploratory data analysis |

---

## Project Structure

```
telecom-churn-analysis/
│
├── data/
│   ├── telco_churn_raw.csv          # Original dataset (Kaggle)
│   └── telco_churn_cleaned.csv      # Cleaned + feature-engineered
│
├── notebooks/
│   └── churn_analysis.ipynb         # Full EDA + cleaning notebook
│
├── churn_analysis.pbix         # Power BI dashboard file
│
└── README.md
```

---

## Dataset

**Source:** [Telco Customer Churn — IBM / Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
**Rows:** 7,043 customers · **Columns:** 21 (original) → 26 (after feature engineering)

**New columns added during cleaning:**
- `TenureBucket` — grouped tenure into 4 lifecycle stages
- `ChargeTier` — Low / Mid / High monthly charge segments  
- `ServiceCount` — number of add-on services per customer
- `ChurnFlag` — binary 0/1 version of Churn for DAX measures
- `AtRisk` — flags active customers with highest churn indicators

---

## How to Run

1. Download the dataset from Kaggle (link above)
2. Run `notebooks/churn_analysis.ipynb` to generate the cleaned CSV
3. Open `churn_analysis.pbix` in Power BI Desktop
4. Refresh the data source to point to your local cleaned CSV path

---

## Skills Demonstrated

- End-to-end analytics workflow (problem → data → insight → action)
- Python data cleaning and feature engineering
- Exploratory data analysis with business framing
- Power BI dashboard design (DAX, slicers, conditional formatting)
- Business communication — findings translated into recommendations

---
