Here is your **README.md content in pure copy-paste format**.
No extra styling, no explanation — **just select all → copy → paste into GitHub**.

---

# 📊 E-Commerce Customer Churn Analysis

*A Complete MySQL Project with Database, Cleaning, Transformation & Churn Insights*

## 📌 Project Overview

Customer churn is a critical metric for e-commerce companies. This project focuses on analyzing churn behavior using SQL, identifying patterns behind customer attrition, and transforming raw transactional data into actionable insights.

This repository contains:

* A fully populated MySQL database (`E-Commerce Customer churn db.sql`)
* SQL script for cleaning, transforming & analyzing churn (`sql assignment 3.sql`)
* The official project instruction PDF

---

## 🗂️ Repository Structure

```
├── E-Commerce Customer churn db.sql
├── sql assignment 3.sql
├── MySQL-E-Commerce Customer Churn Analysis.pdf
└── README.md
```

---

## 🎯 Objectives

### 1️⃣ Build the E-Commerce Customer Churn Database

The file **E-Commerce Customer churn db.sql** includes:

* Database creation
* `customer_churn` table
* 500+ customer records with demographics, device usage, payment modes, complaints, order behavior, and churn labels

---

### 2️⃣ Data Cleaning

Performed using SQL:

* Handle missing values

  * Mean → WarehouseToHome, HourSpendOnApp, OrderAmountHikeFromlastYear, DaySinceLastOrder
  * Mode → Tenure, CouponUsed, OrderCount

* Remove outliers

  * Delete rows where WarehouseToHome > 100

* Fix inconsistent values

  * “Phone” → “Mobile Phone”
  * “Mobile” (order category) → “Mobile Phone”
  * “COD” → “Cash on Delivery”
  * “CC” → “Credit Card”

---

### 3️⃣ Data Transformation

* Rename columns

  * `PreferedOrderCat` → `PreferredOrderCat`
  * `HourSpendOnApp` → `HoursSpentOnApp`

* Create new columns

  * `ComplaintReceived` (Yes/No)
  * `ChurnStatus` (Churned/Active)

* Drop unnecessary columns

  * `Churn`, `Complain`

---

### 4️⃣ Exploratory Data Analysis (EDA)

Includes SQL queries to find:

* Count of churned vs active customers
* Average tenure & cashback of churned customers
* Percentage of churned customers who complained
* City tier with highest churn
* Most preferred payment mode
* Total order amount hike for single mobile users
* Average devices used by UPI customers
* City tier with highest customers
* Gender with highest coupon usage
* Max hours spent by order category
* Order count of credit card users with high satisfaction
* Average satisfaction score for complainers
* Category preferred by >5 coupon users
* Top 3 categories with highest cashback
* Payment modes of customers with tenure 10 and >500 orders
* Distance segmentation & churn breakdown
* Married, Tier-1 customers with above-average orders

---

### 5️⃣ Customer Returns Table

A new table `customer_returns` is created and populated with:

```
ReturnID | CustomerID | ReturnDate | RefundAmount
```

Then a join is performed to display return details of customers who **churned** and **made complaints**.

---

## 🛠️ Technologies Used

* MySQL 8.0+
* SQL (DDL, DML, Aggregations, JOINS, CASE statements)
* E-commerce dataset

---

## ▶️ How to Use

### Step 1 — Clone the Repository

```bash
git clone https://github.com/yourusername/your-repo-name.git
```

### Step 2 — Import the Database

```sql
SOURCE E-Commerce Customer churn db.sql;
```

### Step 3 — Run Assignment Queries

```sql
SOURCE sql assignment 3.sql;
```

### Step 4 — Select the Database

```sql
USE ecomm;
```

---

## 📄 Files Description

| File                                             | Purpose                                     |
| ------------------------------------------------ | ------------------------------------------- |
| **E-Commerce Customer churn db.sql**             | Complete database with all customer records |
| **sql assignment 3.sql**                         | Cleaning, transformation & analysis queries |
| **MySQL-E-Commerce Customer Churn Analysis.pdf** | Project instructions & requirements         |
| **README.md**                                    | Documentation                               |

---

## 🌟 Key Learnings

* SQL data cleaning & preprocessing
* Feature engineering using SQL
* Large dataset EDA
* Payment mode & device preference analysis
* Understanding consumer churn behavior
* Multi-table joins & analytical queries

---
