E-commerce Customer Retention & RFM Analytics
Tools: PostgreSQL, Tableau, Excel/CSV

🚀 Project Overview
This project analyzes a 500k+ row dataset from an Online Retailer to identify growth opportunities. I transformed raw transactional data into actionable business intelligence by calculating Retention Cohorts and RFM segments.

📊 Key Business Questions Answered
Retention: What percentage of customers return after their first month?

Segmentation: Who are our most loyal customers ("Champions"), and who are we about to lose ("At Risk")?

Revenue: Which products and countries drive the highest Average Order Value (AOV)?

🛠️ Data Cleaning Process
To ensure data integrity, the following steps were taken in SQL:

Removed Nulls: Excluded transactions without a Customer ID as they cannot be tracked for retention.

Handled Returns: Identified and isolated negative quantities (returns) to avoid overstating gross revenue.

Type Casting: Converted InvoiceDate from text to TIMESTAMP for time-series analysis.

💡 Business Insights & Recommendations
Insight: Retention peaks in Month 1 but drops by 40% by Month 3.

Recommendation: Implement a "Win-back" email sequence for customers who haven't purchased in 60 days.

Risk: 70% of revenue comes from the top 10% of customers, indicating a high dependency on "Whale" buyers.
