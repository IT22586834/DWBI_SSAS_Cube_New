# DWBI Assignment 02 – SSAS Cube and OLAP Analysis

## 📦 Project Overview

This project showcases the implementation of a **Multidimensional SSAS Cube** and **OLAP reporting** using Excel and Power BI. It extends the data warehouse created in Assignment 01 (OlistDW) using the Brazilian eCommerce dataset. The cube enables deep-dive analysis through slicing, dicing, drill-downs, and drillthroughs.

This project was developed using:
- **Microsoft SQL Server Analysis Services (SSAS)**
- **Microsoft Excel (OLAP)**
- **Power BI Desktop**
- **Visual Studio 2022**

---

## 🎯 Objectives and Learning Outcomes

- Create and deploy a functional SSAS Cube on top of a star-schema data warehouse
- Define hierarchies and attribute relationships for analytical performance
- Demonstrate OLAP operations using Excel and Power BI:
  - Slice, Dice, Roll-up, Drill-down, Drill-through
- Build interactive Power BI dashboards with cascading filters and matrix reports

---

## 🗃️ Data Source

- Dataset: [Brazilian E-Commerce Dataset (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- DW Name: `OlistDW` (built in Assignment 1 via SSIS)
- Star Schema:
  - **Fact Table:** `fact_order_items`
  - **Dimension Tables:** `dim_customer`, `dim_product`, `dim_seller`, `dim_date`

---

## 🔧 Tools and Technologies

| Tool                 | Purpose                                        |
|----------------------|------------------------------------------------|
| SSAS (Multidimensional) | Cube creation, dimension modeling, measure definition |
| Visual Studio 2022   | Cube design and deployment                    |
| Excel                | OLAP browsing and pivot chart operations      |
| Power BI Desktop     | Report creation with advanced interactivity   |
| SQL Server           | Data warehouse hosting                        |

---

## 🧠 SSAS Cube Design

- **Data Source:** `OlistDW` (SQL Server)
- **Data Source View:** Included fact and all dimension tables
- **Dimensions Created:**
  - `dim_customer` – Includes Customer City and State
  - `dim_product` – Includes Product Category
  - `dim_seller` – Includes Seller location
  - `dim_date` – Hierarchy: Year → Quarter → Month
- **Attribute Relationships:** Configured for performance
- **Cube Structure:**
  - **Measure Group:** `fact_order_items`
  - **Measures:** `quantity`, `price`, `freight_value`, `payment_value`, `txn_process_time_hours`
- **Deployment:** Local SSAS server (localhost)

---

## 🧪 Excel OLAP Demonstration

1. Connected to SSAS cube via **Get Data → From Analysis Services**
2. Loaded `fact_order_items` and linked dimensions
3. Built the following OLAP interactions:
   - **Roll-up:** Total payments by Year
   - **Drill-down:** Year → Quarter → Month
   - **Slice:** Product Category & Customer State
   - **Dice:** Combined filters on Product and Date
   - **Pivot:** Visualized row/column changes

---

## 📊 Power BI Reports

### 🧩 Report 1: Matrix Report
- Visualizes Quantity, Price, Freight, and Payment by Product Category
- Slicers: Year and Customer City

### 🧩 Report 2: Cascading Slicers
- Year slicer filters Customer City slicer
- Bar chart: Quantity by Product Category
- Table: Summary metrics

### 🧩 Report 3: Drill-down Report
- Stacked bar chart: Quantity over Year → Quarter → Month

### 🧩 Report 4: Drillthrough Report
- Right-click on a Customer City → navigate to detailed drillthrough page

---

## 📁 Repository Structure

```
├── Document_IT22586834.pdf   # Project documentation (Assignment Report)
├── Report 1.pbix             # Matrix visual Power BI report
├── Report 2.pbix             # Cascading slicer Power BI report
├── Report 3.pbix             # Drill-down Power BI report
├── Report 4.pbix             # Drillthrough Power BI report
```

---

## 👨‍🎓 Author and Academic Info

- **Name:** A.R.S. De Silva  
- **Student ID:** IT22586834  
- **Institution:** Sri Lanka Institute of Information Technology  
- **Course:** Data Warehousing & Business Intelligence (IT3021)  
- **Assignment:** DWBI Assignment 02 – SSAS & OLAP

---
