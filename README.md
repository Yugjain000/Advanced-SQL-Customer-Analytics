# 📊 Customer Intelligence & Sales Analytics Pipeline

## 🎯 Objective
The goal of this project is to transform raw, relational transactional data into actionable business intelligence. By leveraging advanced SQL, this project answers critical business questions regarding customer retention, website conversion drop-offs, and sales team performance. 

## 🛠️ Tech Stack
* **Database:** MySQL 8.0+
* **Data Generation:** Python (`Faker` library) to simulate a realistic dataset of customers, orders, and website events.
* **Core Skills:** Advanced SQL (CTEs, Window Functions, Recursive Queries, Subqueries, Indexing).

## 🗄️ Database Architecture
The database is built on a normalized OLTP schema, tracking both sales transactions and digital user behavior:
* `customers`, `products`, `categories` (Dimension tables)
* `orders`, `order_items` (Fact tables)
* `employees` (Self-referencing table for organizational hierarchy)
* `user_events` (Time-series data tracking website clicks and cart abandonment)

---

## 🚀 Advanced SQL Analytics (Key Highlights)

### 1. RFM Customer Segmentation (Recency, Frequency, Monetary)
Identified the most valuable customers and those at risk of churning by segmenting the customer base into quartiles.
* **SQL Concepts:** `NTILE()` Window Function, Multiple CTEs, `DATEDIFF()`.
* **Business Insight:** Allowed the marketing team to target "Champions" (score 444) with loyalty programs, and "At Risk" customers with win-back email campaigns.
<img width="1167" height="711" alt="image" src="https://github.com/user-attachments/assets/64eb10b2-8916-4a0b-af82-ea3f84c4aaf3" />

### 2. Website Funnel Drop-off Analysis
Analyzed time-series event data to determine exactly where users were abandoning their shopping carts.
* **SQL Concepts:** `LEAD()` and `LAG()` Window Functions, Date/Time manipulation.
* **Business Insight:** Revealed the average time (in minutes) it takes a user to go from `add_to_cart` to `purchase`, highlighting checkout bottlenecks.
<img width="1162" height="803" alt="image" src="https://github.com/user-attachments/assets/723050f8-5e53-4468-b1e2-11640d3e140a" />

### 3. Recursive Sales Hierarchy
Calculated the total revenue generated not just by individual sales reps, but by entire management branches.
* **SQL Concepts:** `WITH RECURSIVE` CTEs, Self-Joins.
* **Business Insight:** Provided executive leadership with a clear view of which regional managers were driving the most indirect sales volume.

---

## 🛡️ How to Run This Project
1. Clone this repository.
2. Run `01_Database_Schema.sql` in MySQL to generate the tables and indexes.
3. Execute `03_Advanced_MySQL_Queries.sql` to view the analytics output.
