🛒 E-Commerce SQL Data Analysis Project

A complete MySQL E-Commerce Analytics Project designed to practice and demonstrate real-world SQL skills including Joins, Aggregations, Subqueries, CTEs, Window Functions, Ranking, Running Totals, Revenue Analysis, Customer Analysis, and Payment Analysis.

The project contains 6 relational tables with 2,600+ records and 25+ SQL business-analysis questions with executable solutions.

────────

📌 Project Overview

This project simulates an e-commerce business where customers place orders for products, employees handle orders, and customers make payments.

The database is designed to answer common business questions such as:

• Which products generate the highest revenue?
• Who are the top customers?
• Which categories perform best?
• Which employees handle the most orders?
• What is the payment success rate?
• How does revenue change month by month?
• Who are the top customers within each city?
• What is the running total of revenue?
• Which products rank highest within their category?

────────

🗂️ Database Structure

The project contains 6 tables:

|Table        |Description                                   |
|-------------|----------------------------------------------|
|`customers`  |Customer personal and location information    |
|`products`   |Product, category, price and stock information|
|`orders`     |Customer orders and order status              |
|`order_items`|Products included in each order               |
|`payments`   |Payment amount, method and status             |
|`employees`  |Employee and department information           |

🔗 Relationship Overview

customers
    │
    │ customer_id
    ▼
orders ─────────────── employees
  │
  │ order_id
  ▼
order_items ───────── products
  │
  │ order_id
  ▼
payments

────────

📊 Dataset Size

|Table      |Records  |
|-----------|--------:|
|Customers  |250      |
|Products   |150      |
|Orders     |500      |
|Order Items|1,209    |
|Payments   |500      |
|Employees  |50       |
|**Total**  |**2,659**|

────────

🛠️ Technologies Used

• MySQL 8.x
• SQL
• MySQL Workbench
• GitHub

────────

🧠 SQL Concepts Covered

Basic SQL

• SELECT
• WHERE
• ORDER BY
• LIMIT
• DISTINCT

Aggregation

• COUNT()
• SUM()
• AVG()
• MIN()
• MAX()
• GROUP BY
• HAVING

Joins

• INNER JOIN
• LEFT JOIN
• Multi-table joins

Advanced SQL

• Subqueries
• CTE (WITH)
• CASE
• COALESCE
• NULLIF
• DATE_FORMAT()

Window Functions

• DENSE_RANK()
• SUM() OVER()
• PARTITION BY
• Running totals
• Category-wise ranking

────────

📈 Business Analysis Performed

👥 Customer Analysis

• Customers by city
• Top customers by spending
• Customers with more than 3 orders
• Customers who never placed an order
• Customer ranking by total spending
• Average order value per customer

📦 Product Analysis

• Most expensive products
• Low-stock products
• Best-selling products
• Product revenue
• Product ranking within category
• Average price by category

💰 Revenue Analysis

• Revenue by category
• Monthly revenue
• Running revenue total
• Revenue contribution percentage
• Highest-revenue category
• Customer-level spending analysis

💳 Payment Analysis

• Payment amount by payment method
• Number of transactions
• Payment success rate
• Payment status distribution

👨‍💼 Employee Analysis

• Orders handled by each employee
• Average employee salary
• Highest-paid employee by department
• Department-wise salary expense
• Employee order-value contribution

────────

📝 SQL Questions Included

The project contains 25 main questions + 5 bonus challenges.

Some examples:

1. Display all customers from Delhi.
2. Find total customers in each city.
3. Find average product price by category.
4. Find the 10 most expensive products.
5. Find products with low stock.
6. Find orders by status.
7. Find orders by source.
8. Calculate revenue by category.
9. Find top 10 customers by spending.
10. Calculate average order value.
11. Find customers with more than 3 orders.
12. Find orders handled by employees.
13. Find employees earning above average salary.
14. Find highest-paid employee in each department.
15. Calculate department-wise salary expense.
16. Find top-selling products.
17. Calculate payments by payment method.
18. Calculate payment success rate.
19. Find customers with no orders.
20. Calculate monthly revenue.
21. Find top 3 customers in each city.
22. Calculate running revenue.
23. Rank products within categories.
24. Calculate category revenue contribution.
25. Create a complete customer-level analytics report.

⭐ Bonus Challenges

• Second-highest priced product in each category
• Customers spending above average
• Highest-value employee orders
• Highest-revenue category by month
• Order-status percentage distribution

────────

🚀 How to Run the Project

Step 1 — Download the SQL file

Download:

sql_6_tables_complete_25_questions_answers.sql

Step 2 — Open MySQL Workbench

Open the .sql file in MySQL Workbench.

Step 3 — Execute the Script

Run the complete script using:

⚡ Run All

The script automatically:

1. Creates the database
2. Creates all 6 tables
3. Creates primary and foreign keys
4. Inserts the dataset
5. Executes the practice/analysis queries

Step 4 — Select the Database

USE ecommerce_practice;

Step 5 — Verify the Data

SELECT COUNT(*) FROM customers;
SELECT COUNT(*) FROM products;
SELECT COUNT(*) FROM orders;
SELECT COUNT(*) FROM order_items;
SELECT COUNT(*) FROM payments;
SELECT COUNT(*) FROM employees;

────────

💡 Example Analysis Query

Revenue by Category

SELECT
    p.category,
    ROUND(
        SUM(
            oi.quantity * p.price *
            (1 - oi.discount_percent / 100)
        ),
        2
    ) AS total_revenue
FROM order_items oi
JOIN products p
    ON oi.product_id = p.product_id
GROUP BY p.category
ORDER BY total_revenue DESC;

────────

📁 Project Files

E-Commerce-SQL-Analytics/
│
├── sql_6_tables_complete_25_questions_answers.sql
└── README.md

────────

🎯 Project Objective

The main objective of this project is to demonstrate the ability to transform relational business data into meaningful insights using SQL.

This project focuses on:

Data → SQL Analysis → Business Insights

It is suitable for practicing SQL for:

• Data Analyst
• Business Analyst
• SQL Developer
• Business Intelligence roles
• Data Science interviews

────────

📌 Key Takeaways

Through this project, the following practical SQL skills are demonstrated:

• Working with relational databases
• Connecting multiple tables using joins
• Performing business aggregations
• Writing nested queries
• Building reusable CTEs
• Using advanced window functions
• Performing ranking analysis
• Calculating running totals
• Performing customer segmentation
• Measuring revenue and payment performance
• Creating business-oriented SQL reports

────────

👨‍💻 Author

Abhinav raj

B.Tech Civil Engineering | Aspiring Data Analyst

Skills

SQL Python Pandas Excel Power BI Data Analysis

────────
