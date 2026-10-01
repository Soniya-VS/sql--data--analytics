# E-Commerce Customer Churn Analysis using MySQL

## 📌 Project Overview

This project focuses on analyzing **customer churn in an e-commerce dataset using MySQL**.

The project involves data cleaning, data transformation, exploratory data analysis, customer behavior analysis, and return/refund analysis to understand patterns associated with customer churn.

## 🛠️ Tools Used

* MySQL
* MySQL Workbench
* SQL

## 📂 Dataset

The dataset contains customer information related to:

* Customer tenure
* Preferred login device
* City tier
* Warehouse distance
* Preferred payment mode
* Gender
* App usage
* Number of registered devices
* Preferred order category
* Satisfaction score
* Marital status
* Number of addresses
* Complaints
* Order amount hike
* Coupon usage
* Order count
* Days since last order
* Cashback amount
* Customer churn

## 🧹 Data Cleaning

The following data-cleaning operations were performed:

* Imputed mean values for:

  * `WarehouseToHome`
  * `HourSpendOnApp`
  * `OrderAmountHikeFromlastYear`
  * `DaySinceLastOrder`
* Imputed mode values for:

  * `Tenure`
  * `CouponUsed`
  * `OrderCount`
* Removed records where `WarehouseToHome > 100`
* Standardized `PreferredLoginDevice`
* Standardized `PreferedOrderCat`
* Standardized payment mode values

## 🔄 Data Transformation

The following transformations were performed:

* Renamed `PreferedOrderCat` to `PreferredOrderCat`
* Renamed `HourSpendOnApp` to `HoursSpentOnApp`
* Created `ComplaintReceived`

  * `Yes` if `Complain = 1`
  * `No` otherwise
* Created `ChurnStatus`

  * `Churned` if `Churn = 1`
  * `Active` otherwise
* Dropped the original `Churn` and `Complain` columns

## 📊 Data Exploration and Analysis

The project answers the following questions:

1. Count of churned and active customers.
2. Average tenure and total cashback amount of churned customers.
3. Percentage of churned customers who complained.
4. City tier with the highest number of churned customers whose preferred order category is Laptop & Accessory.
5. Most preferred payment mode among active customers.
6. Total order amount hike from last year for single customers who prefer mobile phones.
7. Average number of devices registered among customers using UPI.
8. City tier with the highest number of customers.
9. Gender that utilized the highest number of coupons.
10. Number of customers and maximum hours spent on the app in each preferred order category.
11. Total order count for customers who prefer credit cards and have the maximum satisfaction score.
12. Average satisfaction score of customers who complained.
13. Preferred order categories among customers who used more than 5 coupons.
14. Top 3 preferred order categories with the highest average cashback amount.
15. Preferred payment modes of customers whose average tenure is 10 months and who have placed more than 500 orders.
16. Customer churn status based on warehouse distance categories:

* Very Close Distance
* Close Distance
* Moderate Distance
* Far Distance

17. Customer order details for married, City Tier-1 customers whose order count is greater than the average order count.

## ↩️ Customer Returns Analysis

A separate `customer_returns` table was created containing:

* `ReturnID`
* `CustomerID`
* `ReturnDate`
* `RefundAmount`

Return information was then combined with customer information to identify customers who:

* Have churned
* Have made complaints
* Have made returns

## 💡 SQL Concepts Practiced

This project provided practice with:

* `SELECT`
* `WHERE`
* `UPDATE`
* `DELETE`
* `ALTER TABLE`
* `CREATE TABLE`
* `INSERT`
* `JOIN`
* Aggregate functions
* `GROUP BY`
* `ORDER BY`
* `CASE`
* Subqueries
* Conditional filtering
* Data cleaning
* Data transformation
* Customer churn analysis

## 📁 Project Structure

```text
ecommerce-customer-churn-analysis-sql/
│
├── Ecommerce_Customer_Churn_Analysis.sql
└── README.md
```

## 🎯 Objective

The objective of this project is to apply SQL techniques to an e-commerce customer dataset and analyze customer churn, customer behavior, complaints, payment preferences, order patterns, and returns.
