# 🛒 E-Commerce SQL Database Project

## 📌 Project Overview

This project demonstrates the design and implementation of an **E-Commerce Database Management System** using **MySQL**. The database is designed to efficiently manage customers, products, orders, order items, and payment records using relational database concepts.

The project also includes SQL queries to perform business analysis and generate meaningful insights from the data.

---

## 🎯 Project Objectives

- Design a relational database for an e-commerce platform.
- Create normalized database tables.
- Establish relationships using Primary and Foreign Keys.
- Insert sample data into each table.
- Perform business analysis using SQL queries.
- Demonstrate SQL skills for data analysis.

---

## 🛠️ Technologies Used

- MySQL
- MySQL Workbench
- SQL (Structured Query Language)

---

---

## 🗄️ Database Tables

### Customers

Stores customer information.

- Customer_ID
- Customer_Name
- Email
- Phone
- Address
- City

---

### Products

Stores product information.

- Product_ID
- Product_Name
- Category
- Price
- Stock

---

### Orders

Stores customer order details.

- Order_ID
- Customer_ID
- Order_Date
- Order_Status

---

### Order_Item

Stores ordered product information.

- OrderItem_ID
- Order_ID
- Product_ID
- Quantity

---

### Payments

Stores payment details.

- Payment_ID
- Order_ID
- Payment_Mode
- Amount
- Payment_Date
- Payment_Status

---

## 🔗 Database Relationships

```
Customers
     │
     │
   Orders
     │
     │
 Order_Item
   /      \
Products  Payments
```

---

## 📚 SQL Concepts Covered

- CREATE DATABASE
- CREATE TABLE
- INSERT INTO
- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- INNER JOIN
- LEFT JOIN
- Aggregate Functions
- COUNT()
- SUM()
- AVG()
- MAX()
- MIN()
- CASE Statements
- Date Functions
- Primary Key
- Foreign Key

---

## 📊 Business Questions Solved

This project answers important business questions, including:

### Customer Analysis

- Total number of customers
- Customers with multiple orders
- Top customers by order count

### Product Analysis

- Best-selling products
- Least-selling products
- Product-wise sales
- Category-wise products

### Order Analysis

- Total orders
- Delivered orders
- Pending orders
- Cancelled orders
- Monthly order trends

### Revenue Analysis

- Total revenue
- Revenue by product
- Revenue by category
- Average order value

### Payment Analysis

- Total payment amount
- Payment method distribution
- Successful payments
- Failed payments

---

## 💻 Sample SQL Queries

### Total Revenue

```sql
SELECT SUM(Amount) AS Total_Revenue
FROM Payments;
```

### Top Selling Products

```sql
SELECT
P.Product_Name,
SUM(OI.Quantity) AS Total_Sold
FROM Order_Item OI
JOIN Products P
ON OI.Product_ID = P.Product_ID
GROUP BY P.Product_Name
ORDER BY Total_Sold DESC;
```

### Customer with Highest Orders

```sql
SELECT
Customer_ID,
COUNT(Order_ID) AS Total_Orders
FROM Orders
GROUP BY Customer_ID
ORDER BY Total_Orders DESC;
```

---

## 📈 Key Business Insights

The SQL queries provide valuable insights, such as:

- Identify the best-selling products.
- Calculate total business revenue.
- Find the highest-paying customers.
- Analyze customer purchasing behavior.
- Monitor product performance.
- Compare payment methods.
- Track order status.
- Analyze monthly sales trends.
- Identify low-performing products.


## 🎓 Learning Outcomes

Through this project, I learned:

- Relational Database Design
- Database Normalization
- SQL Query Writing
- Table Relationships
- SQL Joins
- Aggregate Functions
- Data Analysis using SQL
- Business Problem Solving
- MySQL Database Management

---

## 💼 Skills Demonstrated

- SQL
- MySQL
- Database Design
- Data Modeling
- Relational Database Management
- Data Analysis
- Query Optimization
- Business Intelligence Concepts
- Problem Solving
- Analytical Thinking

---

## 🔮 Future Enhancements

- Add Views
- Add Stored Procedures
- Add Triggers
- Create Indexes for Performance
- Add More Sample Data
- Implement User Authentication
- Expand Inventory Management


### Skills

- SQL
- MySQL
- Python
- Pandas
- NumPy
- Excel
- Power BI
- Tableau

---

## ⭐ If you found this project helpful

If you like this project, please consider giving it a ⭐ on GitHub.
