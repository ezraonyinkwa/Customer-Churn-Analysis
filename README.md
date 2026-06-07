# Customer Churn Analysis — Financial Services

## What This Project Does

Every financial services business loses customers. The question is 
whether it knows which ones are leaving, why, and what it's costing 
before the damage compounds.

This project analyses churn across a 10,000-customer dataset to 
answer two questions leadership consistently struggles to quantify:

1. **Who is most likely to leave?**
2. **What is their departure actually costing the business?**

The output is two interactive Power BI dashboards — one profiling 
at-risk segments, one translating churn into financial terms.

---

## Business Problem

Despite strong acquisition numbers, the business was experiencing 
steady attrition. Retention strategies existed but lacked focus — 
resources were spread across the entire customer base rather than 
directed at the segments driving the most loss.

Without a data-driven view of churn, two things were happening:
- High-risk customers were not being identified early enough to act
- The revenue cost of churn was invisible, making it easy to 
  underprioritise retention spend

---

## How It Works

### Step 1 — Data Preparation
A dataset of 10,000 customers was cleaned and structured for 
analysis. Customer attributes included:

- Credit Score, Age, Tenure, Balance
- Number of Products, Credit Card Ownership
- Activity Status and Churn Status (Exited)
- Geography and Branch Information

### Step 2 — Data Modelling
A star-schema relational model was built in Power BI with 
**Customer ID** as the primary key across three tables:

| Table | Contents |
|-------|----------|
| **Customer Details** | Demographics, churn status |
| **Region Details** | Geography, branch information |
| **Bank Details** | Balance, products, tenure, credit card ownership |

This structure ensures optimised queries and consistent metrics 
across both dashboards.

### Step 3 — Churn Profiling
Customers were segmented by tenure, age group, activity level, and 
geography to identify which cohorts were churning at above-average 
rates. High-risk profiles were isolated for targeting.

### Step 4 — Financial Impact Modelling
Churned customers were mapped against their account balances and 
product holdings to quantify the deposit loss and revenue 
opportunity cost attributable to attrition.

### Step 5 — DAX Measures & Visualisation
Custom DAX measures were built for:
- Churn rate by segment
- Revenue at risk
- Segment-level KPIs

Results were delivered across two dashboards designed for 
decision-makers, not analysts.

---

## Key Findings

**Who Is Leaving**
- **Early-tenure customers (0–3 years)** show the highest churn — 
  onboarding and early engagement are the critical intervention window
- **The 35–46 age cohort** churns more than any other age group, 
  despite being a high-value demographic
- **Inactive members holding credit cards** are more likely to exit 
  than active members without one — activity level outweighs product 
  ownership as a retention signal
- **Churn rates vary significantly by geography**, pointing to 
  regional service or product fit issues

**What It's Costing**
- High-balance customers are disproportionately represented among 
  those leaving, amplifying the revenue impact of each exit
- Retaining the **top 10% of high-value accounts** could recover a 
  large share of annual deposit leakage
- Even moderate churn among engaged customers compounds into 
  significant revenue loss over a 12-month window

---

## Dashboards

Two interactive dashboards — view and explore them live:

👉 [View Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMjAzMGU1ZTctMmYxMi00YmRhLThlYzctNWE0ZTdmZTg5MDc0IiwidCI6IjU2YjI0YzZhLTczNzEtNDkwOS05ZjliLWI5NmU0YmNlMmZkNiJ9)

**Dashboard 1 — Who Is Leaving**
Segment-level churn breakdown by tenure, age, activity, and geography.

**Dashboard 2 — What It's Costing Us**
Financial impact view mapping churned customers to lost balances 
and revenue at risk.

---

## Tech Stack

- **Power BI** — data modelling, DAX, and dashboard delivery
- **DAX** — churn rate, revenue at risk, and segment KPI measures
- **Star Schema** — relational model across 3 tables
- **Data Cleaning** — preparation and structuring of raw dataset

---

## Who This Is For

This project is relevant to anyone in **retail banking, fintech, or 
financial services** responsible for retention strategy, revenue 
forecasting, or customer analytics. It shows how to move from raw 
customer data to an executive-ready view of churn risk and financial 
exposure — without needing a data engineering team to get there.
