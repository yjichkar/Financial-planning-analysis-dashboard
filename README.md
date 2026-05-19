# Financial Planning & Analysis (FP&A) Dashboard

## Project Overview
The Financial Planning & Analysis (FP&A) Dashboard is an end-to-end business intelligence solution developed using Power BI, SQL, and DAX to analyze and monitor organizational financial performance.

This project helps stakeholders track:
- Revenue growth
- Operational expenses
- Profitability trends
- Budget vs Actual performance
- Cash flow movement
- Forecasting insights
- Department-wise financial efficiency

The dashboard automates financial reporting workflows and provides interactive analytics to support data-driven business decision-making.

---

# Business Problem
Organizations often rely on manual Excel-based financial reporting processes that:
- consume significant time,
- increase reporting inconsistencies,
- make variance tracking difficult,
- and limit visibility into financial trends.

The objective of this project was to centralize financial reporting, automate KPI calculations, and create executive-level dashboards for faster and more accurate decision-making.

---

# Objectives
The project focuses on:

- Monitoring revenue, expenses, profitability, and cash flow trends
- Performing budget vs actual variance analysis
- Building forecasting and trend analysis reports
- Automating financial KPI reporting
- Improving reporting accuracy using SQL and DAX
- Creating interactive executive dashboards

---

# Tech Stack

| Technology | Purpose |
|---|---|
| Power BI | Dashboard development & visualization |
| SQL | Data extraction, cleaning & analysis |
| DAX | KPI calculations & financial metrics |
| Excel / CSV | Source financial datasets |
| Power Query | Data transformation |
| Data Modeling | Relationship management & schema design |

---

# Dataset
The project uses financial budgeting and variance analysis datasets from Kaggle.

Dataset includes:
- Revenue
- Expenses
- Budgeted Amount
- Actual Amount
- Departments
- Financial Categories
- Monthly Transactions
- Profit Metrics
- Regional Data

---

# Data Preparation & Transformation

Data transformation was performed using Power Query and SQL.

## Key Transformation Steps
- Removed duplicate records
- Handled missing values
- Standardized date formats
- Validated financial amounts
- Created calculated financial columns
- Merged budget and actual datasets
- Generated monthly and yearly financial aggregations

---

# Data Model

The dashboard follows a star schema model.

## Fact Tables
- Financial Transactions
- Budget Data
- Actual Financials

## Dimension Tables
- Date Dimension
- Department Dimension
- Region Dimension
- Financial Category Dimension

This structure improves:
- query performance,
- scalability,
- and reporting efficiency.

---

# Dashboard Features

## 1. Executive Summary Dashboard

### KPIs
- Total Revenue
- Total Expenses
- Net Profit
- Profit Margin %
- Cash Flow
- Budget Utilization %
- Variance %

### Visualizations
- Revenue Trend Analysis
- Expense Distribution
- Monthly Profitability
- Cash Flow Trend
- KPI Cards
- Year-over-Year Growth

---

## 2. Budget vs Actual Analysis

This page compares planned financial performance against actual business outcomes.

### Metrics
- Budgeted Revenue
- Actual Revenue
- Budget Variance
- Variance Percentage
- Department Variance

### Business Insights
- Over-budget departments
- Underperforming business units
- Monthly financial deviation analysis

---

## 3. Profitability Analysis Dashboard

Focused on measuring organizational profitability.

### Metrics
- Gross Profit
- Net Profit
- Operating Margin
- Profit Margin %
- Department Profitability

### Insights Generated
- High-cost operational areas
- Most profitable departments
- Expense-heavy business segments
- Margin improvement opportunities

---

## 4. Cash Flow Analysis

Tracks organizational cash movement trends.

### KPIs
- Cash Inflow
- Cash Outflow
- Net Cash Flow
- Monthly Cash Balance

### Visualizations
- Monthly cash flow trend
- Cash inflow vs outflow
- Seasonal financial movement

---

## 5. Forecasting Dashboard

Forecasting was implemented using Power BI analytics and trend analysis.

### Forecast Metrics
- Revenue Forecast
- Expense Forecast
- Profit Forecast
- Growth Projection

### Forecasting Insights
- Future revenue trends
- Seasonal expense patterns
- Financial growth prediction

---

# DAX Measures Used

## Financial KPIs
- Revenue
- Expenses
- Net Profit
- Profit Margin %
- Variance %
- Budget Achievement %
- Running Totals
- Year-over-Year Growth

## Example DAX Measures

### Profit Margin
```DAX
Profit Margin % =
DIVIDE([Net Profit], [Revenue], 0) * 100
```

### Variance
```DAX
Variance =
SUM(Financials[Actual Amount]) -
SUM(Financials[Budget Amount])
```

### Variance %
```DAX
Variance % =
DIVIDE([Variance],
SUM(Financials[Budget Amount]),0) * 100
```

### YoY Growth
```DAX
YoY Growth % =
DIVIDE(
[Current Year Revenue] - [Previous Year Revenue],
[Previous Year Revenue],0
) * 100
```

---

# SQL Operations Performed

The project uses SQL for:
- data validation,
- financial aggregation,
- KPI extraction,
- and reporting optimization.

## SQL Concepts Used
- Aggregations
- GROUP BY
- JOINS
- Common Table Expressions (CTEs)
- Window Functions
- Data Cleaning Queries

## Sample SQL Query

```sql
SELECT
    Month,
    SUM(Revenue) AS Total_Revenue,
    SUM(Expenses) AS Total_Expenses,
    SUM(Revenue - Expenses) AS Net_Profit
FROM financial_data
GROUP BY Month
ORDER BY Month;
```

---

# Business Impact

The FP&A dashboard improved financial reporting capabilities by:

- Reducing manual reporting effort
- Improving financial reporting accuracy
- Increasing visibility into revenue and expense trends
- Supporting strategic financial planning
- Enabling faster executive decision-making
- Automating recurring KPI reporting workflows

---

# Project Structure

```bash
financial-planning-analysis-dashboard/
│
├── dataset/
│   ├── budget_vs_actual.csv
│   └── financial_data.xlsx
│
├── dashboard/
│   └── fpanda_dashboard.pbix
│
├── sql/
│   ├── financial_queries.sql
│   └── variance_analysis.sql
│
├── screenshots/
│   ├── executive_dashboard.png
│   ├── variance_dashboard.png
│   ├── profitability_dashboard.png
│   └── cashflow_dashboard.png
│
├── README.md
└── requirements.txt
```

---

# Dashboard Preview

## Executive Dashboard
(Add Screenshot Here)

## Variance Analysis Dashboard
(Add Screenshot Here)

## Profitability Dashboard
(Add Screenshot Here)

## Cash Flow Dashboard
(Add Screenshot Here)

---

# Future Enhancements
- Real-time database integration
- Predictive analytics using Python
- Automated email reporting
- Role-based dashboard access
- AI-powered financial forecasting

---

# Conclusion
This project demonstrates practical experience in:
- Financial analytics
- Business intelligence
- Power BI dashboard development
- SQL-based financial analysis
- DAX calculations
- KPI automation
- Data modeling
- Executive reporting

The dashboard provides actionable financial insights and supports data-driven strategic planning through interactive visual analytics.
