# Zepto E-Commerce SQL Data Analyst Portfolio Project

## 📌 Project Overview
This project is a **real-world SQL Data Analyst portfolio project** based on an e-commerce inventory dataset from **Zepto**, one of India’s fastest-growing quick-commerce platforms.

The objective of this project is to simulate how data analysts work in **retail and e-commerce companies**, using SQL to explore data, clean messy datasets, and generate business-driven insights.

This project is suitable for:
- 📊 Data Analyst / Business Analyst aspirants
- 📚 Learners practicing SQL with real-world data
- 💼 Interview preparation for retail, e-commerce, and product analytics roles

---

## 🛠 Tools & Technologies Used
- PostgreSQL  
- SQL  
- pgAdmin  

---

## 📁 Dataset Description
- Source: Kaggle (scraped from Zepto product listings)
- Each record represents a **unique SKU (Stock Keeping Unit)**
- Duplicate product names exist due to different sizes, weights, discounts, or categories — similar to real e-commerce catalog data

### 🧾 Columns
- `sku_id` – Unique product identifier  
- `name` – Product name  
- `category` – Product category  
- `mrp` – Maximum Retail Price (₹)  
- `discountPercent` – Discount applied on MRP  
- `discountedSellingPrice` – Final selling price after discount (₹)  
- `availableQuantity` – Inventory units available  
- `weightInGms` – Product weight in grams  
- `outOfStock` – Stock availability flag  
- `quantity` – Units per package  

---

## 🧱 Database Schema
```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);
