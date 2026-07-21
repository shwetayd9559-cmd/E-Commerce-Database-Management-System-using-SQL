🛒 E-Commerce Database Management System using SQL

📌 Project Overview

This project demonstrates the design and implementation of an E-Commerce Database Management System using MySQL. The database is designed to manage customers, products, orders, order items, and payments while maintaining proper relationships using primary and foreign keys.
The project also includes SQL queries that generate valuable business insights from the stored data.

🎯 Project Objectives

- Design a relational database for an e-commerce platform.
- Create normalized tables with proper relationships.
- Insert sample data into each table.
- Perform data analysis using SQL queries.
- Generate business insights from sales, customers, products, and payments.
  
🛠️ Technologies Used

- MySQL
- MySQL Workbench
- SQL

🗂 Database Tables

The project consists of five relational tables:

Customers

Stores customer information.

Customer_ID
Customer_Name
Email
Phone
Address
City
Products

Stores product details.

Product_ID
Product_Name
Category
Price
Stock
Orders

Stores customer order details.

Order_ID
Customer_ID
Order_Date
Order_Status
Order_Item

Stores ordered products.

OrderItem_ID
Order_ID
Product_ID
Quantity
Payments

Stores payment details.

Payment_ID
Order_ID
Payment_Mode
Amount
Payment_Date
Payment_Status
🔗 Database Relationships
Customers
     │
     │
   Orders
     │
     │
 Order_Item
   /      \
Products  Payments
💡 SQL Concepts Used
CREATE DATABASE
CREATE TABLE
INSERT INTO
PRIMARY KEY
FOREIGN KEY
SELECT
WHERE
ORDER BY
GROUP BY
HAVING
INNER JOIN
LEFT JOIN
Aggregate Functions
COUNT()
SUM()
AVG()
MIN()
MAX()
CASE Statements
Date Functions
📊 Business Questions Solved

The SQL queries answer important business questions, including:

Customer Analysis
Total number of customers
Customers with multiple orders
Customers who placed the highest number of orders
Product Analysis
Best-selling products
Least-selling products
Product-wise sales
Category-wise products
Order Analysis
Total orders
Delivered orders
Pending orders
Cancelled orders
Monthly order trends
Sales Analysis
Total revenue
Revenue by product
Revenue by category
Average order value
Payment Analysis
Total payment amount
Payment method distribution
Successful payments
Failed payments

📈 Sample SQL Queries

Total Revenue

SELECT SUM(Amount) AS Total_Revenue
FROM Payments;

Top Selling Products

SELECT
P.Product_Name,
SUM(OI.Quantity) AS Total_Sold
FROM Order_Item OI
JOIN Products P
ON OI.Product_ID = P.Product_ID
GROUP BY P.Product_Name
ORDER BY Total_Sold DESC;

Customer with Highest Orders

SELECT
Customer_ID,
COUNT(Order_ID) AS Total_Orders
FROM Orders
GROUP BY Customer_ID
ORDER BY Total_Orders DESC;

📊 Key Business Insights

Using SQL queries, the following insights can be generated:

Identify top-selling products.
Calculate total business revenue.
Find the highest-paying customers.
Analyze order status distribution.
Compare payment methods used by customers.
Monitor product performance.
Track monthly sales trends.
Identify products with low sales.
Evaluate customer purchasing behaviour.
