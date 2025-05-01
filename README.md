
# Task 6 - Sales Trend Analysis Using SQL

## 📌 Objective
To analyze **monthly revenue** and **order volume** using SQL queries on a sales dataset.

## 🛠 Tools Used
- MySQL Workbench
- SQL
- Public dataset: Superstore Sales Data

## 🗃 Dataset Details
We used a Superstore-style dataset that contains:
- `order_id` (Unique ID for each order)
- `order_date` (Date when the order was placed)
- `amount` (Total sales amount)
- `product_id` (ID of the product sold)

## 🔍 SQL Queries Used

### 1️⃣ Monthly Revenue and Order Volume
```sql
SELECT
    DATE_FORMAT(order_date, '%Y-%m') AS month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS total_orders
FROM
    orders
GROUP BY
    month
ORDER BY
    month;
