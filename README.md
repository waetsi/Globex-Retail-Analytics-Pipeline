# Globex Retail Analytics Pipeline

## Project Overview

This project analyses a fictional retail dataset (Globex Retail) using Python and Pandas.
The work is structured as a clear analytics pipeline, progressing from raw data understanding to business-ready insights.

The goal is not just to analyse data, but to demonstrate good analytics practice, reproducibility, and reasoning at each stage.

---

## Project Structure

```text
Globex-Retail-Analytics-Pipeline/
│
├── 01_globex_retail_data_familiarisation.ipynb
├── 02_globex_retail_data_cleaning.ipynb
├── 03_globex_retail_feature_engineering.ipynb
├── 04_globex_retail_eda_kpis.ipynb
│
├── outputs/
│   ├── globex_retail_clean.csv
│   ├── globex_retail_features.csv
│   └── globex_retail_customer_metrics.csv
│
└── README.md
```

Each notebook represents a distinct milestone, and each milestone is committed separately to GitHub.

---

## Milestone 1 — Data Familiarisation

Notebook: `01_globex_retail_data_familiarisation.ipynb`

In this stage, I explored the raw dataset to understand:

* What each row represents (a single retail transaction)
* Dataset size and structure
* Column meanings and data types
* Missing values and early data quality risks

Key outcome:
The dataset contains 5,000 clean transaction records with no missing values.
Potential transformation needs (such as date parsing) were identified but not applied at this stage.

---

## Milestone 2 — Data Cleaning & Validation

Notebook: `02_globex_retail_data_cleaning.ipynb`

This milestone focused on **proving the data was analysis-ready**, not assuming it.

Key steps included:

* Converting `Order_Date` to a proper datetime format
* Validating discount values (stored as decimal rates)
* Verifying revenue calculations using business logic
* Checking for duplicates and impossible values (e.g. negative prices)

Key outcome:
The dataset required minimal correction, but all assumptions were validated.
A clean dataset was exported for downstream analysis.

Output:

* `outputs/globex_retail_clean.csv`

---

## Milestone 3 — Feature Engineering

**Notebook:** `03_globex_retail_feature_engineering.ipynb`

Here, the cleaned transactional data was enhanced with new analytical features, including:

 Time-based features (month, weekday)
 Order-level metrics (gross sales, discount amount, net sales)
 Customer-level aggregations (total revenue, average order value)
 Customer segmentation into `High_Value` and `Standard` groups

Key outcome:
The dataset was transformed from raw transactions into an insight-ready format, supporting customer and trend analysis.

Outputs:

 `outputs/globex_retail_features.csv`
 `outputs/globex_retail_customer_metrics.csv`

---

## Milestone 4 — Exploratory Data Analysis & KPIs

Notebook: `04_globex_retail_eda_kpis.ipynb`

This final stage answers business-focused questions, including:

Revenue contribution by product category
 Top product sub-categories by revenue
 Average order value by customer segment
 Monthly revenue trends

Key insights:

 Electronics is the dominant revenue category
 High_Value customers spend approximately 5× more per order** than Standard customers
 Monthly revenue trends reveal clear performance patterns over time

These insights are supported by summary tables and a simple time-series visualisation.

---

## Key Skills Demonstrated

* Python (Pandas, Matplotlib)
* Data cleaning and validation
* Feature engineering
* Exploratory data analysis
* KPI development
* Version control with Git & GitHub
* Structured, milestone-based workflow

---

## Notes

* This project prioritises **clarity, reasoning, and reproducibility** over complex modelling.
* Each milestone is intentionally committed separately to reflect a real analytics workflow.