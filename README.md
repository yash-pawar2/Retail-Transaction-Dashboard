<div align="center">

# 🛒 Retail Transaction Analytics Dashboard
### End-to-End Power BI Case Study · 1M+ Records · 2020–2024

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://microsoft.com/excel)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)]()
[![Dataset](https://img.shields.io/badge/Rows-1%2C000%2C000-blueviolet?style=for-the-badge)]()

![GitHub last commit](https://img.shields.io/github/last-commit/yash-pawar2/Retail-Transaction-Dashboard)

> Transforming **1 million raw retail transactions** into actionable business intelligence — uncovering seasonal trends, store-level performance gaps, and promotion ROI across a 5-year multi-city dataset.

</div>

---

## 📌 Problem Statement

Retail businesses operating across multiple cities and store formats often struggle to answer three critical questions:

- **Where** is revenue concentration risk highest?
- **When** should promotional budgets be deployed for maximum ROI?
- **Who** are the high-value customer segments, and what drives their behavior?

This project builds a scalable Power BI solution that answers all three — using a real-world 1M-row transaction dataset spanning 5 years, 3 store types, and multiple product categories.

---
## 🗂 Dataset Overview

| Property | Details |
|----------|---------|
| **File** | `Retail_Transactions.csv` |
| **Volume** | 1,000,000 rows · ~13M total data points |
| **Timespan** | 2020 – 2024 |
| **Key Columns** | `Transaction_ID` · `Date` · `Product` · `Category` · `Total_Items` · `Total_Cost` · `Payment_Method` · `City` · `Store_Type` · `Discount_Applied` · `Customer_Category` · `Season` · `Promotion` |

---

## 🎯 Business Objectives

| # | Objective | Analytical Approach |
|---|-----------|-------------------|
| 1 | Track monthly revenue and volume trends | Time-series line charts with YoY comparison |
| 2 | Compare store-type and city-level performance | Filled map + ranked bar charts |
| 3 | Measure promotional campaign effectiveness | Pre/post promotion lift analysis |
| 4 | Understand customer purchase patterns | RFM-style segmentation + payment behavior |

---

## ⚙️ Analytical Workflow

### 1 · Data Cleaning & Validation
- Identified and removed null/duplicate records across 13M data points
- Resolved inconsistent date formats and standardized categorical fields (`Store_Type`, `Season`, `Category`)
- Validated referential integrity between transaction IDs and customer/product dimensions
- Applied consistent naming conventions to enable reliable cross-filter behavior in Power BI

### 2 · Data Modeling
- Designed a **star schema** with fact table (`Transactions`) and dimension tables (`Product`, `Store`, `Customer`, `Date`)
- Built a custom **Date Intelligence table** using DAX for YTD, QTD, and MoM calculations
- Created 15+ DAX measures including:
  - `Total Revenue`, `Total Items Sold`, `Average Order Value`
  - `Promotion Lift %`, `Season-over-Season Growth`
  - `Customer Retention Rate` by segment and store type

### 3 · Dashboard Design
- Applied **Z-pattern visual hierarchy** for executive-readability
- Synchronized slicers (City, Season, Store Type, Year) across all report pages
- Used conditional formatting to surface outliers and underperformers instantly

---


## 📈 Key Insights & Business Impact

### 💰 Revenue Performance

| KPI | Value | Insight |
|-----|-------|---------|
| Total Revenue (2020–2024) | **$52.46M** | ~11.4% CAGR — growth sustained through pandemic and inflation cycles |
| Total Items Sold | **5.50M units** | ~1.1M units/year · avg. 92K items/month |
| Average Orders per Customer | **52** | Weekly purchase cadence — signals highly loyal, habitual buyer base |
| Revenue per Item | **$9.54** | Consistent with FMCG-led category mix |

### 🍂 Seasonality Findings

Fall is the single highest-ROI period across all five years — outperforming the annual average by **~18%**. 🏪 Store Comparison | Horizontal bar | Which store format is most efficient per transaction? |

**Recommendation:** Concentrate 60–70% of annual promotional budget in the Fall window (late September–November). Pre-position inventory 6–8 weeks ahead to prevent stockout-driven revenue loss at peak demand.

### 🏬 Store Type Analysis

| Store Type | Frequency | Avg Basket | Strategic Role |
|------------|-----------|------------|---------------|
| Supermarket | High (weekly) | Moderate | Volume driver — protect loyalty here |
| Pharmacy | Medium | Low–moderate | Necessity hedge — stable in downturns |
| Warehouse Club | Low | High | Margin driver — upsell opportunity |

**Finding:** The three-format mix creates a natural revenue hedge. When discretionary warehouse spending softens, pharmacy necessity purchases hold — reducing overall revenue volatility.

---

## 🔍 Analytical Decisions & Trade-offs

> This section documents *why* specific choices were made — not just *what* was built.

- **Star schema over flat table:** Enabled faster DAX calculations and cleaner cross-filtering at 1M+ row scale; the trade-off was slightly more complex ETL but significantly better dashboard performance.
- **Custom date table over auto date/time:** Power BI's built-in auto date/time creates hidden tables per column — at this data volume, a single explicit date table reduced model size by ~40%.
- **Season as a filter vs. calculated column:** Stored Season as a dimension attribute rather than computing it dynamically in DAX — reduces query overhead across 1M rows on every slicer interaction.
- **Fall insight validation:** Cross-validated the Fall growth finding across all 5 years independently before including it as a headline insight — confirmed consistent +15–21% lift in each year, not a single-year anomaly.

---

## 🧰 Tools & Technologies

| Tool | Version | Role |
|------|---------|------|
| **Power BI Desktop** | Latest | Dashboard, DAX modeling, visualization |
| **Microsoft Excel** | 365 | Initial data profiling, cleaning validation |
| **Power Query (M)** | — | ETL pipeline, data transformation |
| **DAX** | — | KPI measures, time intelligence, segmentation |

---

## 📎 Project Files
- 📊 **Download Power BI File (.pbit)**  
- 📄 **View Dataset (.zip)**  

---

## 👤 Author
**Yash Pawar**  
🎯 *Aspiring Data Analyst | Power BI & SQL Enthusiast | MIT-WPU*  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yash-pawar2/)  [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/yash-pawar2)  [![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:Yash.r.pawar246@gmail.com)
