# E-commerce Customer Retention & RFM Analytics

> End-to-End Analytics Pipeline for Customer Lifetime Value & RFM Segmentation
> Tools: PostgreSQL, Tableau, Excel/CSV, Python

## 🚀 Project Overview

This project analyzes a 500k+ row dataset from an Online Retailer to identify growth opportunities. 
I transformed raw transactional data into actionable business intelligence by calculating Retention Cohorts and RFM segments.

## Data Overview
- Dataset: UCI Online Retail II (2009-2011).
- Type: Transactional E-commerce data.
- Size: ~1,000,000+ rows (across two sheets/years).
- Content: Invoice, StockCode, Description, Quantity, InvoiceDate, Price, CustomerID, Country.




## 🛠️ Pipline Process
1. Data Preparation
   1. using excel to export two sheets in xlsx to csv. Loaded two csv to databse using pgAdmin import function.
   2. using python script to read both sheet as dataframe and then concate them in to one dataframe, passed it to the database using sqlalchemy package.
2. 


To ensure data integrity, the following steps were taken in SQL:

- Removed Nulls: Excluded transactions without a Customer ID as they cannot be tracked for retention.

- Handled Returns: Identified and isolated negative quantities (returns) to avoid overstating gross revenue.

- Type Casting: Converted InvoiceDate from text to TIMESTAMP for time-series analysis.

## 📊 Key Business Questions Answered
- Retention: What percentage of customers return after their first month?

- Segmentation: Who are our most loyal customers ("Champions"), and who are we about to lose ("At Risk")?

- Revenue: Which products and countries drive the highest Average Order Value (AOV)?

## 💡 Business Insights & Recommendations
> Insight: Retention peaks in Month 1 but drops by 40% by Month 3.

-  Recommendation: Implement a "Win-back" email sequence for customers who haven't purchased in 60 days.

-  Risk: 70% of revenue comes from the top 10% of customers, indicating a high dependency on "Whale" buyers.

