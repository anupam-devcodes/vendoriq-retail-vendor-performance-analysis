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

### 1. Data Ingestion

Multiple raw CSV files were loaded into an SQLite database using Python and SQLAlchemy.

Using a relational database made it easier to manage large datasets, perform joins, create reusable analytical tables, and maintain a structured analysis workflow.

### 2. SQL Exploration and Transformation

SQL was used to:

- Explore database tables and understand their relationships
- Identify missing, duplicated, and inconsistent values
- Join purchasing, sales, vendor, pricing, and inventory data
- Aggregate vendor- and brand-level performance
- Create a consolidated `Vendor Sales Summary` table for further analysis

### 3. Exploratory Data Analysis

Python and Pandas were used to:

- Analyze data distributions and outliers
- Evaluate vendor and brand performance
- Measure purchasing concentration
- Analyze inventory turnover
- Identify low-sales, high-margin brands
- Study relationships between sales, purchases, costs, and profitability

### 4. Statistical Validation

Confidence intervals and hypothesis testing were used to compare profitability between vendor groups and determine whether the observed differences were statistically meaningful.

### 5. Power BI Dashboard

The final analytical dataset was imported into Power BI to create an interactive dashboard containing:

- Executive KPI cards
- Top vendor and brand rankings
- Vendor purchase concentration
- Inventory turnover analysis
- Unsold inventory capital
- Profitability and sales opportunity analysis

---

## 🛠️ Technology Stack

| Category | Tools |
|---|---|
| Programming | Python |
| Data Manipulation | Pandas, NumPy |
| Database | SQLite |
| Database Integration | SQLAlchemy |
| Querying and Transformation | SQL |
| Data Visualization | Matplotlib, Seaborn |
| Statistical Analysis | SciPy |
| Dashboarding | Microsoft Power BI, DAX |
| Development Environment | Jupyter Notebook |
| Version Control | Git, GitHub |

---

## 📁 Project Structure

```text
VendorIQ/
│
├── assets/
│   └── vendoriq_dashboard.png
│
├── data/
│   └── raw CSV files
│
├── database/
│   └── vendor_inventory.db
│
├── notebooks/
│   ├── 01_data_ingestion.ipynb
│   ├── 02_database_exploration.ipynb
│   └── 03_vendor_performance_eda.ipynb
│
├── sql/
│   └── vendor_sales_summary.sql
│
├── dashboard/
│   └── VendorIQ_Dashboard.pbix
│
├── reports/
│   └── vendor_performance_report.pdf
│
├── README.md
├── requirements.txt
└── .gitignore
```

> Raw datasets and the generated SQLite database are excluded from GitHub because of file-size and data-distribution constraints.

---

## 📊 Dashboard Components

### Executive KPI Cards

The dashboard tracks the following business metrics:

- Total Sales
- Total Purchases
- Gross Profit
- Profit Margin
- Unsold Inventory Capital

### Vendor Performance

Vendor performance is evaluated using:

- Total sales
- Total purchases
- Gross profit
- Profit margin
- Purchase contribution
- Inventory turnover

### Brand Performance

The dashboard identifies:

- Top-selling brands
- Low-sales, high-margin brands
- Brands requiring pricing adjustments
- Products with potential promotional opportunities

### Inventory Analysis

Inventory efficiency is monitored using:

- Stock turnover
- Unsold inventory value
- Slow-moving vendors
- Capital locked in inventory

---

## 📐 Power BI Measures

The following DAX measures were used to calculate the major dashboard KPIs.

```DAX
Total Sales =
SUM('VendorSalesSummary'[TotalSalesDollars])
```

```DAX
Total Purchases =
SUM('VendorSalesSummary'[TotalPurchaseDollars])
```

```DAX
Gross Profit =
SUM('VendorSalesSummary'[GrossProfit])
```

```DAX
Profit Margin % =
DIVIDE(
    [Gross Profit],
    [Total Sales],
    0
)
```

```DAX
Unsold Inventory Capital =
SUM('VendorSalesSummary'[UnsoldInventoryValue])
```

```DAX
Average Stock Turnover =
AVERAGE('VendorSalesSummary'[StockTurnover])
```

> Table and column names may need to be adjusted according to the final Power BI data model.

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/anupam-devcodes/VendorIQ.git
cd VendorIQ
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS/Linux

```bash
source venv/bin/activate
```

### 4. Install the required dependencies

```bash
pip install -r requirements.txt
```

### 5. Add the source datasets

Place the required CSV files inside the following directory:

```text
data/
```

The raw datasets are not included in the repository.

### 6. Run the notebooks in sequence

Run the notebooks in the following order:

```text
notebooks/01_data_ingestion.ipynb
notebooks/02_database_exploration.ipynb
notebooks/03_vendor_performance_eda.ipynb
```

### 7. Open the Power BI dashboard

Open the following file using Microsoft Power BI Desktop:

```text
dashboard/VendorIQ_Dashboard.pbix
```

Update the local data-source path if required.

---

## ✅ Business Recommendations

Based on the analysis, the following actions are recommended:

1. **Promote high-margin brands with low sales**

   Develop targeted promotional campaigns, improve product visibility, and evaluate pricing for the 198 identified brands.

2. **Reduce vendor concentration risk**

   Explore alternative suppliers and gradually diversify purchases to reduce dependence on the top 10 vendors.

3. **Use bulk purchasing strategically**

   Larger orders provide lower unit costs, but purchase volumes should be aligned with demand forecasts and inventory capacity.

4. **Reduce slow-moving inventory**

   Review reorder quantities, introduce clearance strategies, and avoid excessive purchasing from low-turnover vendors.

5. **Improve vendor negotiation strategies**

   Use purchasing volume, profitability, and inventory performance to negotiate better pricing and contract terms.

6. **Support high-margin, low-volume vendors**

   Investigate whether low sales are caused by limited market reach, weak distribution, insufficient promotion, or pricing issues.

7. **Monitor unsold inventory continuously**

   Track inventory capital through the Power BI dashboard to identify slow-moving products before they become a major financial risk.

---

## 🎓 Skills Demonstrated

This project demonstrates practical experience in:

- Translating business problems into analytical questions
- Building an end-to-end analytics workflow
- Ingesting multiple datasets into a relational database
- Writing SQL joins, aggregations, CTEs, and transformations
- Creating a consolidated analytical data model
- Performing exploratory data analysis
- Detecting outliers and analyzing distributions
- Conducting confidence interval and hypothesis testing
- Developing business KPIs
- Building an interactive Power BI dashboard
- Communicating insights through business recommendations
- Organizing and documenting an analytics project on GitHub

---

## ⚠️ Limitations

- The analysis is based on historical data and does not establish causality.
- Vendor performance may also be affected by seasonality, location, promotions, customer demand, and market conditions.
- Profitability calculations depend on the purchasing and sales fields available in the source dataset.
- Operating expenses, logistics costs, and contractual terms may not be included.
- The complete raw dataset is not publicly included in the repository.

---

## 🔮 Future Improvements

Potential future enhancements include:

- Vendor risk scoring
- Product-level demand forecasting
- Sales and purchase trend analysis over time
- Reorder-point recommendations
- Inventory optimization models
- Seasonal product analysis
- Geographic performance analysis
- Automated database refreshes
- Automated Power BI dataset refreshes
- Power BI Service deployment
- Vendor segmentation using machine-learning techniques

---

## 👨‍💻 Author

### Anupam Choubey

Final-year engineering student focused on data analytics, business intelligence, SQL, Python, and analytical problem-solving.

- **GitHub:** [anupam-devcodes](https://github.com/anupam-devcodes)
- **Project:** VendorIQ — Retail Vendor Performance & Profitability Intelligence

---

<div align="center">

### ⭐ If you found this project useful, consider giving the repository a star.

**Built with SQL, Python, statistical analysis, and Power BI.**

</div>

