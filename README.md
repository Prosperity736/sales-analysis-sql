# sales-analysis-sql
# 📌 Sales Analysis Using SQL

## 🎯 Business Problem
Retail companies often struggle to identify trends in their sales data. This project analyzes a year’s worth of sales transactions to uncover key insights like:
- What regions generate the most revenue?
- Who are the top-performing sales reps?
- Which product categories bring in the most money?
- What are the monthly sales trends?

Understanding this helps businesses improve marketing, staffing, and inventory decisions.

---

## 📊 Dataset
This dataset simulates retail sales for 2023, covering 100 transactions across multiple regions and products.

🔗 [Download Dataset](./data/sales_data.csv)

*Columns include:*
- OrderID: Unique transaction ID
- OrderDate: Date of sale
- Region: Geographic sales region
- SalesRep: Name of the salesperson
- ProductName, Category: Item details
- UnitPrice, Quantity: Pricing info
- TotalPrice: Auto-calculated revenue from sale

---

## ⚙ SQL Concepts Used
This project used several SQL concepts to analyze the data:
- `JOIN`s (if multiple tables are used later)
- Aggregate functions: SUM(), AVG(), COUNT()
- GROUP BY, ORDER BY, and HAVING
- Filtering with WHERE and CASE
- Date functions: MONTH(), YEAR(), DATEPART()
- Common Table Expressions (CTEs)

---

## 🔍 Example Insights & Queries
Here are some questions this project answers using SQL:

1. *Total Revenue by Region*
```sql
SELECT Region, SUM(TotalPrice) AS TotalRevenue
FROM sales_data
GROUP BY Region
ORDER BY TotalRevenue DESC;

SELECT ProductName, SUM(Quantity) AS UnitsSold
FROM sales_data
GROUP BY ProductName
ORDER BY UnitsSold DESC
LIMIT 5;

SELECT 
  STRFTIME('%m', OrderDate) AS Month,
  SUM(TotalPrice) AS MonthlyRevenue
FROM sales_data
GROUP BY Month
ORDER BY Month;

🧠 What I Learned
	•	How to explore sales data using raw SQL
	•	Writing complex queries using grouping, filtering, and date functions
	•	Structuring queries for business storytelling
	•	Creating insights from a flat dataset with no need for joins
	•	Understanding how to turn simple tables into actionable insights

Project Structure
/sales-analysis-sql
│
├── data/
│   └── sales_data.csv
│
├── queries/
│   └── sales_queries.sql
│
├── README.md

💼 Author

Prosper Onwuzirike
Beginner SQL & Data Analysis Portfolio Project
GitHub Profile

