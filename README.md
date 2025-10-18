# 🍔 Customers Food Order Pattern Analysis

## 📘 Project Overview
The **Customers Food Order Pattern Analysis** project focuses on analyzing customer ordering behavior from multiple food outlets such as **KFC**, **Pizza Hut**, and **Dominos**.  
Using **SQL**, this project explores order frequency, billing patterns, and outlet-wise preferences to uncover meaningful insights about customer behavior and business performance.

---

## 🧰 Tools Used
- **SQL (MySQL)**
  - Data Cleaning & Transformation  
  - Window Functions  
  - Joins and Subqueries  
  - Aggregate & Analytical Queries

---

## 📊 Key Objectives
1. Identify and remove **duplicate orders** from the dataset.  
2. Retrieve the **latest order details** per customer using ranking functions.  
3. Generate **cumulative sales and order counts** for each outlet.  
4. Compare **customer ordering frequency** across multiple restaurants.  
5. Analyze **total spending patterns** by outlet and customer.  

---

## 🧮 Database & Tables
- **Database:** `mdr`  
- **Table:** `swiggy`  

### Columns:
| Column Name   | Description                          |
|----------------|--------------------------------------|
| `ID`           | Record identifier                    |
| `Cust_ID`      | Unique customer code                 |
| `Order_ID`     | Unique order number                  |
| `Partner_code` | Restaurant partner identifier        |
| `Outlet`       | Restaurant name (KFC, Pizza Hut, Dominos) |
| `Bill_Amount`  | Order value in INR                   |
| `Order_Date`   | Date of order placed                 |
| `Comments`     | Delivery feedback or issue remarks   |

---

## 🧩 SQL Tasks & Queries

### **Q1: Find count of duplicate rows**
Identified duplicate order records using `GROUP BY` and `HAVING` clauses.

### **Q2: Remove duplicate records**
Created a temporary table with distinct values and re-created the `swiggy` table to retain only unique records.

### **Q3: Retrieve records from position 4 to 9**
Used the `LIMIT` clause to extract specific record ranges.

### **Q4: Find the latest order placed by each customer**
Applied **window function (`RANK()`)** with partitioning by `Cust_ID` to fetch the most recent orders.

### **Q5: Replace blank comments with 'No Issues'**
Used `UPDATE` statements with conditional logic for text replacement.

### **Q6: Calculate cumulative sales and order count by outlet**
Used **user-defined variables** to compute running totals of orders and revenue.

### **Q7: Customer visit frequency across outlets**
Aggregated the number of orders each customer placed per outlet (KFC, Dominos, Pizza Hut).

### **Q8: Customer spending by outlet**
Summed up total **bill amounts** per customer per outlet to identify high-value customers.

---

## 💡 Key Insights
- Duplicate records were successfully removed, ensuring data consistency.  
- **KFC** had the highest order count, while **Pizza Hut** generated higher total sales.  
- **Customer SW1005** was one of the most active repeat customers across multiple outlets.  
- Most customers placed **2–3 repeat orders** within a 3-month window.  
- Cumulative sales analysis showed steady order growth towards year-end.  

---

## 🧾 Conclusion
This project demonstrates how **SQL** can be leveraged to analyze food ordering data efficiently, detect patterns, and ensure data accuracy.  
The insights derived from customer behavior and outlet performance can help food delivery businesses improve **customer retention, order accuracy, and operational planning**.

---

## 🧑‍💻 Author
**Manjunath Darshan R**

📧 *[rmanjunathdarshan@gmail.com]*  
💼 *[https://www.linkedin.com/in/manjunathdarshanr/]*  
_Data Analyst | SQL | Excel | Power BI | Python_
