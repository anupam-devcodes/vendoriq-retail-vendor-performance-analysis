<div align="center">

# 📊 VendorIQ

### Retail Vendor Performance & Profitability Intelligence

An end-to-end data analytics project that transforms purchasing, sales, vendor, and inventory data into actionable business insights using **SQL, Python, statistical analysis, and Power BI**.

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

## 📌 Project Overview

Retail and wholesale businesses depend heavily on vendors for product availability, pricing, inventory flow, and profitability.

Poor vendor decisions can lead to:

- Excess inventory and increased holding costs
- Low-margin product sales
- Slow inventory turnover
- Overdependence on a small group of suppliers
- Inefficient purchasing and pricing decisions

**VendorIQ** analyzes vendor-level purchasing, sales, profitability, and inventory performance to help stakeholders make better decisions related to vendor management, pricing, procurement, and inventory optimization.

---

## 🎯 Business Objectives

This project focuses on answering the following business questions:

1. Which vendors contribute the most to sales, purchases, and gross profit?
2. Which brands have low sales but high profit margins?
3. Does bulk purchasing reduce the average unit purchase cost?
4. Which vendors are associated with slow-moving inventory?
5. How concentrated is purchasing among the top vendors?
6. Is there a significant profitability difference between high-performing and low-performing vendors?

---

## 📊 Power BI Dashboard

<!-- Place the dashboard screenshot inside: assets/vendoriq_dashboard.png -->

<p align="center">
  <img src="assets/vendoriq_dashboard.png" alt="VendorIQ Power BI Dashboard" width="100%">
</p>

The interactive Power BI dashboard provides stakeholders with a consolidated view of:

- Total sales, purchases, gross profit, and profit margin
- Unsold inventory capital
- Top-performing vendors and brands
- Purchase concentration among major vendors
- Low inventory turnover vendors
- Low-sales, high-margin product opportunities

---

## 🔑 Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Sales | **$441.41M** |
| Total Purchases | **$307.34M** |
| Gross Profit | **$134.07M** |
| Overall Profit Margin | **38.7%** |
| Unsold Inventory Capital | **$2.71M** |
| Top 10 Vendor Purchase Contribution | **65.69%** |
| Low-Sales, High-Margin Brands | **198** |

---

## 💡 Key Business Insights

### 1. High-margin brands with growth potential

The analysis identified **198 brands** with low sales but comparatively high profit margins.

These brands may benefit from:

- Targeted promotional campaigns
- Improved product visibility
- Better distribution
- Controlled pricing adjustments

---

### 2. High vendor concentration

The top 10 vendors account for **65.69% of total purchases**, while all remaining vendors contribute only 34.31%.

This indicates significant supplier concentration and creates potential risks related to:

- Supply-chain disruptions
- Reduced negotiation power
- Vendor dependency
- Pricing pressure

---

### 3. Bulk purchasing significantly reduces unit cost

| Order Size | Average Unit Purchase Cost |
|---|---:|
| Small Orders | **$39.06** |
| Medium Orders | **$15.49** |
| Large Orders | **$10.78** |

Large purchase orders resulted in an approximately **72% lower average unit cost** compared with small orders.

This demonstrates the financial advantage of bulk purchasing when supported by reliable demand forecasts and sufficient inventory capacity.

---

### 4. Unsold inventory is locking working capital

Approximately **$2.71M** is tied up in unsold inventory.

Slow-moving inventory can result in:

- Higher storage costs
- Reduced cash flow
- Product obsolescence
- Lower inventory efficiency

Vendors with low inventory turnover should be reviewed for lower reorder quantities, promotional strategies, or purchasing adjustments.

---

### 5. Low-performing vendors are not always low-margin vendors

| Vendor Group | Mean Profit Margin |
|---|---:|
| High-performing Vendors | **31.17%** |
| Low-performing Vendors | **41.55%** |

Low-performing vendors generated higher average profit margins but lower overall sales.

This suggests that their weaker performance may be caused by limited demand, poor distribution, lower market reach, or ineffective pricing rather than low profitability.

---

## 📈 Statistical Analysis

The project uses statistical methods to validate findings rather than relying only on descriptive analysis.

Techniques used include:

- Descriptive statistics
- Distribution analysis
- Outlier detection
- Correlation analysis
- Confidence intervals
- Independent sample t-tests
- Vendor profitability comparison

The statistical analysis was used to compare profit margins between high-performing and low-performing vendor groups and determine whether the observed difference was statistically meaningful.

---

## 🔄 Project Workflow

```mermaid
flowchart LR
    A[Raw CSV Files] --> B[Python Data Ingestion]
    B --> C[SQLite Database]
    C --> D[SQL Exploration and Cleaning]
    D --> E[Vendor Sales Summary]
    E --> F[Python EDA]
    F --> G[Statistical Analysis]
    G --> H[Business Insights]
    H --> I[Power BI Dashboard]
    I --> J[Business Recommendations]
