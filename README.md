# 🧾 Olist Brazilian E-commerce Data Wrangling

## Overview

This project focuses on transforming a **multi-table Brazilian e-commerce dataset (Olist)** into a structured, analysis-ready format.

The primary objective is to combine fragmented transactional data, engineer meaningful features, and enable business-level insights such as revenue distribution, customer value, and category performance.

---

## Business Context

E-commerce platforms often store data across multiple tables (orders, customers, products, transactions).
To derive actionable insights, this data must be:

* Integrated into a unified structure
* Cleaned and transformed
* Aggregated at meaningful levels (customer, order, category, city)

This project addresses these challenges using structured data wrangling techniques.

---

## Dataset

* **Source:** Olist Brazilian E-commerce Dataset (Kaggle: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
* Includes multiple relational tables:

  * Customers
  * Orders
  * Order Items
  * Products
  * Product Category Translations

---

## Approach

### 1. Data Integration (Merging)

* Combined multiple datasets using appropriate join operations:

  * Orders + Order Items
  * Products + Category Translations
  * Integrated with Customers
* Created a **master dataset** representing complete transactional information

---

### 2. Feature Engineering

* Derived key business metric:

  * **Total Order Value = Price + Freight Value**
* Aggregated:

  * Total value per order
  * Total value per customer
  * Total revenue per product category

---

### 3. Analytical Transformations

* Identified **top customers** based on spending
* Analyzed **category-level revenue contribution**
* Built grouped datasets for further analysis

---

### 4. Pivot Tables & Aggregation

* Created pivot tables for:

  * Revenue by product category
  * Revenue by customer city
* Enabled multi-dimensional analysis of sales performance

---

### 5. Data Reshaping

* Converted wide-format pivot tables into **long format** using `melt()`
* Prepared data for downstream tasks such as visualization and modeling

---

## Key Highlights

* Integrated multiple relational datasets into a unified structure
* Applied structured data wrangling techniques using Pandas
* Engineered business-relevant metrics for analysis
* Enabled multi-level aggregation (customer, category, city)

---

## Outcome

The project results in a clean, structured dataset that supports:

* Customer segmentation
* Revenue analysis
* Category performance evaluation
* Geographic sales insights

This forms a strong foundation for further visualization and machine learning tasks.

---

## Project Structure

```bash id="olist-structure"
olist-ecommerce-data-wrangling/
│
├── olist-brazillian-ecommerce-data-wrangling.ipynb
├── dataset/
    └── olist_orders_dataset.csv
    └── olist_order_items_dataset.csv
    └── olist_customers_dataset.csv
    └── olist_products_dataset.csv
    └── product_category_name_translation.csv
```

---

## Conclusion

This project demonstrates how effective data wrangling transforms fragmented raw data into meaningful, analysis-ready information. It highlights the importance of structured data preparation in real-world data science workflows.

---

## Note

This repository focuses on the **data wrangling and transformation aspect**. Visualization and advanced analysis are handled separately.
