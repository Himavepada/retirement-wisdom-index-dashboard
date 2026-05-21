# Retirement Readiness Analytics — Wisdom Index Dashboard

**Tools:** Power BI · DAX · Power Query (M) · Python · Excel  
**Domain:** Financial Planning & Advisory  
**Timeline:** Aug – Dec 2025 (MS Capstone Project, University of North Texas)

---

## Problem statement

Financial advisors at Wisdom Index struggled to assess whether clients would be financially ready to retire comfortably at age 67 and maintain their lifestyle through age 95. Client data was fragmented across multiple sources, making holistic evaluation time-consuming and inconsistent.

**Goal:** Build an integrated, interactive Power BI dashboard that calculates a personalized "Wisdom Index" score for each client — consolidating financial, behavioral, and planning data into a single actionable view.

---

## What I built

An end-to-end analytics solution covering:

- **ETL pipeline** using Power Query (M) to consolidate multi-source client data from Salesforce CRM into a unified 71-variable master dataset
- **30+ custom DAX measures** implementing proprietary Wisdom Index financial formulas
- **Interactive Power BI dashboard** with client-level filtering and scenario planning
- **Python EDA** for data quality validation and outlier detection

---

## Methodology

### 1. Data collection & integration
- Source: Salesforce CRM client records (6 clients, 71 variables each)
- Variables: demographics, income, assets, liabilities, insurance coverage, behavioral attributes, and financial goals
- ETL: Power Query (M) to standardize column names, consolidate linked records, and resolve data type issues

### 2. Data cleaning & quality
- Identified and resolved missing values in spouse birthdates, tuition fields, and purchase totals using subject-matter estimates and central tendency measures
- Applied **Winsorization** on Total Value and Annual Premium to handle outliers without distorting trends
- Standardized all financial values for cross-client comparability

### 3. Python EDA
- Histograms and KDE plots for net worth distribution
- Boxplots to detect outliers in Annual Premium
- Scatterplots: Years Employed vs. Total Value (positive correlation confirmed)
- Bar charts: Home Value by client for comparative analysis

### 4. DAX modeling
Built 30+ measures across key categories:

| Measure category | Examples |
|---|---|
| Aggregations | Total Assets, Total Annual Income, Total Liabilities |
| Ratios & Indices | Savings Percentage, Debt-to-Value Ratio, Reserves in Months |
| Gap analysis | Retirement Funding Gap, Total Variance from Goal |
| Goal tracking | Cashflow Goals, Living Expense % vs. 40% target |

All measures validated against manual calculations for 100% numerical accuracy.

### 5. Dashboard design
- Client lookup filter for instant per-client views
- Scenario planner: adjustable rate of return and monthly contribution inputs
- KPI cards surfacing Retirement Funding Gap, Savings Rate, Net Margin
- Recommended Actions panel linking underperforming metrics to corrective guidance

---

## Key findings

- **Retirement Funding Gap:** –$18.47M for the sample client — significant shortfall requiring immediate advisor intervention
- **Behavioral factors matter:** Clients with longer employment histories had significantly higher asset accumulation (confirmed via scatterplot analysis)
- **Protection gaps identified:** Life Insurance, Disability Insurance, and LTC showed $0 coverage for certain clients — high risk exposure flagged for advisor follow-up
- **High variability** in client profiles confirmed that one-size-fits-all financial advice is ineffective — segmented, personalized strategies are essential

---

## Files in this repository

| File | Description |
|---|---|
| `python_eda.ipynb` | Python notebook: data exploration, outlier detection, visualizations |
| `README.md` | Project documentation |

> **Note:** The Power BI .pbix dashboard file and client dataset are not included in this repository due to client data confidentiality.

---

## Skills demonstrated

`Power BI` `DAX` `Power Query (M)` `Python` `Pandas` `Matplotlib` `Seaborn` `ETL` `Data Cleaning` `Financial Modeling` `Salesforce CRM` `Data Storytelling` `Scenario Analysis`
# retirement-wisdom-index-dashboard
