# Customer Churn Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results / Findings](#results--findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)

---

## Project Overview

This customer churn analysis project was developed to analyze customer behavior, churn patterns, and retention metrics using Power BI.

The goal of the project is to help business and customer success teams monitor key churn KPIs, identify at risk customer segments, and understand the major factors driving churn through interactive dashboards and data-driven insights.

---

## Data Sources

### Telecom Dataset
### Customer Dataset
The dataset used in this project is the **Databel-Data** Excel file, which contains customer-related information such as demographics, subscription details, usage behavior, service interactions, and churn status — designed to simulate real-world customer churn analytics scenarios.


### Dataset Fields Include
- `CustomerID` – Unique customer identifier
- `Churn Label` – Whether the customer churned (Yes/No)
- `Churn Reason` – Customer-reported reason for leaving
- `Contract Type` – Month-to-month, one year, two year
- `Age` – Customer age
- `Payment Method` – Payment method used by the customer
- `International Plan` – Whether the customer has an international plan
- `Customer Service Calls` – Number of calls made to customer service

---

## Tools

- **Power BI** – Dashboard creation and reporting
- **Power Query** – Data cleaning and transformation
- **DAX** – KPI calculations and analytics
---

## Data Cleaning & Preparation

In the data preparation phase, the following steps were performed:

- Loaded dataset into Power BI
- Checked and corrected data types
- Renamed columns for clarity
- Created calculated columns for age groups and churn categories
- Handled missing values and inconsistencies

---

## Exploratory Data Analysis

EDA was performed to answer important business questions such as:

- What is the overall customer churn rate?
- Which customer segments have the highest churn?
- How does tenure affect the likelihood of churn?
- What are the most common reasons customers leave?
- How does contract type or payment method relate to churn?

---

## Data Analysis

Created multiple DAX measures and calculations including:

```DAX
Total Customers = COUNT('Databel-Data'[Customer ID])

Churn Rate % =
DIVIDE([Churned Customers], [Total Customers])
```

### DAX Functions Used
- CALCULATE()
- DIVIDE()
- IF()
- COUNT()
- SWITCH()

### Dashboards Created
- Overview Dashboard (churn rate, churn reasons, geographic map)
- Demographics Dashboard (age groups, senior citizens, churn reasons)
- Contract Type Dashboard (contract type, payment method, account length)
- Intl Calls Dashboard (intl plan, intl active)
- Unlimited Plan Dashboard (unlimited data plan status, consumption)

---

## Results / Findings

The analysis revealed the following insights:

- The dataset contains over **6,600+ customers**
- Approximately **27% of customers have churned**
- Month-to-month contract customers show significantly higher churn rates
- Customers with shorter tenure are most likely to churn
- Top churn reasons include competitor offers, pricing dissatisfaction, and poor support experience
---

## Recommendations


Based on the analysis, the following recommendations were identified:

- Introduce loyalty programs targeting customers in their first year
- Offer competitive pricing or discounts to customers flagged as at-risk
- Improve customer support quality and response times
- Promote annual or two-year contracts with incentives over month-to-month plans
- Use churn risk dashboards to enable proactive outreach by customer success teams
---

## Limitations

- Dataset is fictional and intended for analytics practice purposes
- Some churn drivers (e.g., personal reasons) may not be captured in the data
- Analysis is based on historical records and does not account for real-time changes


---

## Future Improvements

Potential future enhancements include:

- Predictive churn modeling using machine learning
- Customer lifetime value (CLV) integration
- Real-time churn risk scoring
- Cohort analysis for deeper retention insights
- Drill-through pages by customer segment or region

---
