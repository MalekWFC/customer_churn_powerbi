# Customer Churn Analysis: Telecom Insights Dashboard

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

This customer churn analysis project was developed to investigate churn rates and uncover the key reasons why customers are leaving a telecom service, using Power BI.

The goal of the project is to help business teams understand churn behavior, identify high-risk customer segments, and take data-driven action to improve customer retention through interactive dashboards and visual storytelling.

The project includes data transformation, DAX measures and calculated columns, exploratory analysis, and multi-page dashboard design.

---

## Data Sources

### Telecom Dataset
The dataset used in this project is a fictional telecom dataset from **Databel**, designed to simulate real-world customer churn scenarios. It contains customer-related information such as demographics, contract types, payment methods, international and data plan usage, and churn status used to analyze churn behavior and retention trends.

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
- **DAX** – KPI calculations and churn metrics
- **Data Visualization** – Interactive report pages and storytelling

---

## Data Cleaning & Preparation

In the data preparation phase, the following steps were performed:

- Loaded dataset into Power BI
- Checked and corrected data types
- Renamed columns for clarity
- Created calculated columns for age groups and churn categories
- Validated data integrity and checked for missing values

---

## Exploratory Data Analysis

EDA was performed to answer important business questions such as:

- What is the overall churn rate for Databel?
- What are the most common reasons customers are churning?
- Which age groups have the highest churn rates?
- How does contract type affect churn?
- Does having an international or unlimited data plan influence churn?
- Which states or regions have higher churn concentrations?

---

## Data Analysis

Created multiple DAX measures and calculated columns including:

```DAX
Number of Customers = COUNT(Databel[Customer ID])

Churned Customers = CALCULATE(COUNT(Databel[Customer ID]), Databel[Churn Label] = "Yes")

Churn Rate = DIVIDE([Churned Customers], [Number of Customers])
```

### DAX Functions Used
- CALCULATE()
- DIVIDE()
- IF()
- COUNT()
- SWITCH()

### Dashboards Created
- Overview Dashboard (churn rate, churn reasons, geographic map)
- Demographics Dashboard (age groups, gender, senior citizens)
- Plan & Contract Dashboard (contract type, payment method, international & data plans)

---

## Results / Findings

The analysis revealed the following insights:

- Databel's overall churn rate is approximately **26.86%**
- The top churn reason is **competitor offerings** — better devices and better deals
- Customers on **month-to-month contracts** churn at significantly higher rates than those on annual contracts
- **Senior citizens (65+)** have a notably higher churn rate compared to younger age groups
- Customers with an **international plan who are not on an international calling group** show very high churn
- **Direct debit** payment method correlates with higher churn rates
- Customers making **frequent customer service calls** are more likely to churn

---

## Recommendations

Based on the analysis, the following recommendations were identified:

- Offer incentives to convert month-to-month customers to longer-term contracts
- Investigate and improve the international plan pricing and offerings to reduce churn in that segment
- Design targeted retention campaigns for senior citizen customers
- Reduce friction in customer service by addressing common pain points that drive repeated service calls
- Benchmark against competitors on device offerings and pricing to reduce competitor-driven churn
- Monitor customers on direct debit with high service usage as an early churn-risk signal

---

## Limitations

- Dataset is fictional and created for analytics practice purposes
- Churn reasons are self-reported and may not fully reflect true customer motivations
- Analysis is based on a static snapshot and does not account for changes over time

---

## Future Improvements

Potential future enhancements include:

- Predictive churn modeling using machine learning
- Customer lifetime value (CLV) integration
- Real-time churn monitoring dashboard
- Cohort analysis to track retention over time
- Drill-through pages for individual customer profiles

---
