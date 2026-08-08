# Finance Data Analysis

End-to-end exploratory data analysis, cleaning, standardization, feature engineering, and visualization on a real-world, messy finance transactions dataset.

## Objective

Take a raw, inconsistent transactions dataset and turn it into a clean, standardized, analysis-ready dataset — then surface business insights through aggregation and visualization.

## Dataset

**Source:** [finance_dirty_data_1.csv](https://raw.githubusercontent.com/vinothsivaperumal/eda/refs/heads/main/finance_dirty_data_1.csv) — a public, intentionally messy synthetic finance transactions dataset (inconsistent casing, missing values, duplicate rows, malformed emails) designed for EDA/cleaning practice.

**Scale:** 5,002 rows, 15 columns — Transaction_ID, Transaction_Date, Customer_Name, City, Account_Type, Transaction_Type, Channel, Status, Amount, Fee, Balance, Credit_Score, Customer_Age, Risk_Score, Email.

## Pipeline

1. **Data Discovery** — shape, dtypes, summary statistics, missing values, unique category values, duplicate detection.
2. **Data Cleaning** — dropped duplicates, filled missing numeric fields with median (Amount, Balance, Credit_Score), filled missing emails with a placeholder, converted dates to datetime, fixed malformed email domains.
3. **Data Standardization** — normalized column names to lowercase/underscore, trimmed and title-cased text fields (customer_name, city, account_type, transaction_type, channel, status) to remove inconsistent casing and whitespace.
4. **Feature Engineering** — derived `year`, `month_num`, `month_name`, `net_amount` (amount − fee), and `fee_percentage`.
5. **Aggregation** — total amount by city/account type, average balance by channel, top 10 customers by transaction amount.
6. **Data Enrichment** — rule-based `amount_band` (High/Medium/Low) and `credit_segment` (Excellent/Good/Fair/Poor) classifications.
7. **Visualization** — monthly transaction trend (line chart), total amount by city (bar chart), account type contribution (pie chart).

## Repo structure

```
data/                          Raw dataset (finance_dirty_data_1.csv)
Finance_Data_Analysis.ipynb    Full analysis notebook (37 questions, executed with outputs)
```

## Tools

Python · pandas · NumPy · Matplotlib · Seaborn · Jupyter/Google Colab

## Notes

Questions 29, 33, and 34 from the original assignment were not captured in the source material used to reconstruct this notebook.
