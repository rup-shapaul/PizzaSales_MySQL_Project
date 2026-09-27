# 🍕 Pizza Sales Data Analysis Using MySQL

## 📌 Project Overview

This project focuses on analyzing pizza sales data using **MySQL** to extract meaningful business insights from transactional data.

The analysis involves multiple relational tables containing information about orders, pizza details, pizza types, categories, prices, quantities, and order timings. SQL queries were used to explore sales performance, customer ordering patterns, revenue contribution, and product performance.

The main objective of this project is to demonstrate practical **SQL and Data Analytics skills** by transforming raw sales data into useful business insights.

---

## 🎯 Project Objectives

The project aims to answer important business questions such as:

* How many orders were placed?
* What is the total revenue generated?
* Which pizza has the highest price?
* Which pizza size is ordered most frequently?
* What are the most ordered pizza types?
* Which pizza categories generate the highest quantity of sales?
* At what time of the day are orders most frequently placed?
* What is the average number of pizzas ordered per day?
* Which pizza types generate the most revenue?
* What percentage of revenue comes from each pizza category?
* How does revenue accumulate over time?
* Which are the top-performing pizzas within each category?

---

## 🗂️ Dataset Structure

The database contains the following main tables:

### 1. `orders`

Contains information about individual orders.

| Column       | Description                        |
| ------------ | ---------------------------------- |
| `order_ID`   | Unique ID of the order             |
| `order_date` | Date on which the order was placed |
| `order_time` | Time at which the order was placed |

### 2. `order_details`

Contains details about pizzas included in each order.

| Column             | Description                   |
| ------------------ | ----------------------------- |
| `order_details_ID` | Unique ID for order detail    |
| `order_Id`         | ID of the corresponding order |
| `pizza_Id`         | ID of the pizza               |
| `quantity`         | Quantity of pizzas ordered    |

### 3. `pizzas`

Contains information about individual pizza products.

This table includes attributes such as:

* Pizza ID
* Pizza type ID
* Pizza size
* Pizza price

### 4. `pizza_types`

Contains information about different pizza types.

This table includes:

* Pizza type ID
* Pizza name
* Pizza category

---

## 🛠️ Tools & Technologies

* **MySQL**
* SQL
* Relational Database Management
* Data Analysis

---

## 📊 SQL Analysis Performed

### 1. Total Number of Orders

Calculated the total number of orders placed using the `COUNT()` function.

### 2. Total Revenue

Calculated total revenue using:

```text
Quantity × Pizza Price
```

and aggregated the result using `SUM()`.

### 3. Highest-Priced Pizza

Identified the pizza with the highest price by joining the `pizza_types` and `pizzas` tables and sorting prices in descending order.

### 4. Most Common Pizza Size

Analyzed order details by pizza size to determine which size was ordered most frequently.

### 5. Top 5 Most Ordered Pizza Types

Calculated the total quantity sold for each pizza type and identified the top 5 based on quantity ordered.

### 6. Pizza Category Sales

Analyzed the total quantity of pizzas ordered for each category.

### 7. Orders by Hour

Used MySQL's `HOUR()` function to analyze how orders are distributed throughout the day.

### 8. Pizza Category Distribution

Calculated the number of pizza types belonging to each category.

### 9. Average Pizzas Ordered Per Day

Grouped orders by date and calculated the average number of pizzas ordered per day.

### 10. Top 3 Pizza Types by Revenue

Identified the three pizza types generating the highest revenue.

### 11. Revenue Contribution

Calculated the percentage contribution of each pizza category to the overall revenue.

### 12. Cumulative Revenue Analysis

Used a **window function** to calculate cumulative revenue over time.

### 13. Top 3 Pizzas Within Each Category

Used the `RANK()` window function with `PARTITION BY` to identify the top 3 pizza types based on revenue within each category.

---

## 🧠 SQL Concepts Used

This project demonstrates several important SQL concepts used in real-world data analysis:

* `SELECT`
* `WHERE`
* `COUNT()`
* `SUM()`
* `AVG()`
* `ROUND()`
* `GROUP BY`
* `ORDER BY`
* `LIMIT`
* `JOIN`
* Subqueries
* Aggregate Functions
* Date & Time Functions
* Window Functions
* `SUM() OVER()`
* `RANK() OVER()`
* `PARTITION BY`

---

## 🔍 Key Analytical Areas

The analysis focuses on four major areas:

### 📦 Order Analysis

Understanding order volume and ordering patterns throughout the day.

### 🍕 Product Analysis

Identifying popular pizza sizes, pizza types, and categories.

### 💰 Revenue Analysis

Measuring total revenue, revenue by pizza type/category, and cumulative revenue.

### 📈 Performance Analysis

Identifying the highest-performing pizza products and comparing their performance within categories.

---

## 📁 Project Structure

```text
Pizza-Sales-SQL-Analysis/
│
├── dataset/
│   ├── orders.csv
│   ├── order_details.csv
│   ├── pizzas.csv
│   └── pizza_types.csv
│
├── Pizza_Sales_Analysis.sql
│
└── README.md
```

> Update the folder/file names above if your actual GitHub repository uses different names.

---

## 🚀 How to Run the Project

### Step 1: Install MySQL

Install MySQL and a MySQL client such as **MySQL Workbench**.

### Step 2: Create the Database

Run:

```sql
CREATE DATABASE Pizzahut;
USE Pizzahut;
```

### Step 3: Import the Dataset

Import the required CSV files into the corresponding tables:

* `orders`
* `order_details`
* `pizzas`
* `pizza_types`

### Step 4: Run the SQL Script

Open:

```text
Pizza_Sales_Analysis.sql
```

and execute the queries in MySQL Workbench.

---

## 📌 What This Project Demonstrates

Through this project, I practiced using SQL to:

* Work with relational datasets
* Combine data using multiple-table joins
* Perform exploratory data analysis
* Calculate sales and revenue metrics
* Identify top-performing products
* Analyze time-based ordering patterns
* Use subqueries for analytical calculations
* Apply window functions for advanced analysis
* Convert raw transactional data into business-oriented insights

---

## 👩‍💻 Author

**Rupsha Paul**

B.Tech — Computer Science & Engineering

Interested in **Data Analytics, SQL, Excel, Power BI, and Business Intelligence**.

---

⭐ If you find this project useful, feel free to explore the SQL queries and analysis.
