# E-commerce Customer Retention & RFM Analytics

> Tools: PostgreSQL, Tableau, Excel/CSV

## 🚀 Project Overview

This project analyzes a 500k+ row dataset from an Online Retailer to identify growth opportunities. 
I transformed raw transactional data into actionable business intelligence by calculating Retention Cohorts and RFM segments.

## 📊 Key Business Questions Answered
- Retention: What percentage of customers return after their first month?

- Segmentation: Who are our most loyal customers ("Champions"), and who are we about to lose ("At Risk")?

- Revenue: Which products and countries drive the highest Average Order Value (AOV)?

## 🛠️ Data Cleaning Process
>- 🛠 Data Integrity Audit
Before analysis, the raw dataset contained 541,909 records. After performing a data audit, I identified three main issues:

Missing Identity: 24% of rows lacked a Customer ID. These were excluded from the retention study but kept for gross revenue snapshots.

Transactional Anomalies: 10,000+ rows contained negative quantities (returns). I moved these to a separate returns table to analyze churn.

Final Scope: The cleaned dataset for the RFM model consists of 406,829 high-integrity rows.



To ensure data integrity, the following steps were taken in SQL:

- Removed Nulls: Excluded transactions without a Customer ID as they cannot be tracked for retention.

- Handled Returns: Identified and isolated negative quantities (returns) to avoid overstating gross revenue.

- Type Casting: Converted InvoiceDate from text to TIMESTAMP for time-series analysis.

## 💡 Business Insights & Recommendations
> Insight: Retention peaks in Month 1 but drops by 40% by Month 3.

-  Recommendation: Implement a "Win-back" email sequence for customers who haven't purchased in 60 days.

-  Risk: 70% of revenue comes from the top 10% of customers, indicating a high dependency on "Whale" buyers.

