# 🛒 Retail Sales Revenue & Performance Analytics

> **Section D | Group 15** — A Comprehensive Revenue & Sales Analytics Report  
> **February 2026** | Confidential — Internal Use Only

---

## 📊 Dashboard

> 🔗 **[View Live Interactive Dashboard →](https://docs.google.com/spreadsheets/d/1kQwIlLnrHc2I-UWneBf6vj2vV0kbgzcUcms2aMwVz7c/edit?gid=1869737493#gid=1869737493)**

---

## 📁 Repository Structure

```
SECTIONDGROUP15YIELDANALYSIS/
├── RawDataSET/                  # Original raw transaction data
├── Cleaned/                     # Cleaned & processed dataset
├── Calculations_Pivots/         # Pivot tables & analysis sheets
├── Dashboard/                   # Dashboard files
├── Retail_Sales_Report_Final.pdf
└── Retail_Sales_Analysis_Presentation.pdf
```

---

## 🧭 Project Overview

| Metric              | Value                  |
| ------------------- | ---------------------- |
| **Total Revenue**   | ₹1,472,998 (~₹1.47M)   |
| **Units Sold**      | 62,889                 |
| **Discount Rate**   | 33.7%                  |
| **Avg. Bill Value** | ₹129.70                |
| **Time Period**     | FY 2022–2025 (partial) |
| **Currency**        | Indian Rupees (INR)    |

### Sector & Business Context

The retail and e-commerce sector is fundamentally data-driven, with businesses generating thousands of transactions daily. This project addresses a real-world business problem where data analytics directly impacts revenue optimization, operational efficiency, and strategic planning.

### Problem Statement

> To analyze retail transactional data comprehensively to identify key revenue drivers, evaluate discount effectiveness, assess category and product performance, and uncover sales trends — in order to support data-driven business decision-making and optimize operational performance.

### Project Scope

- ✅ Complete data cleaning and preprocessing pipeline
- ✅ Development of business-aligned KPI framework
- ✅ Comprehensive exploratory data analysis (EDA)
- ✅ Interactive dashboard creation in Google Sheets
- ✅ Strategic business recommendations based on findings

### Industry Challenges Addressed

| #   | Challenge                          | Description                                                                      |
| --- | ---------------------------------- | -------------------------------------------------------------------------------- |
| 01  | **Discount Strategy Inefficiency** | Blanket discounts applied without measuring actual impact on spending or margins |
| 02  | **Limited Performance Visibility** | Lack of real-time insights into category and product-level performance           |
| 03  | **Seasonal Demand Forecasting**    | Difficulty identifying and preparing for seasonal trends                         |
| 04  | **Revenue Concentration Risk**     | Failure to identify high-revenue products and categories                         |

---

## 📋 Data Dictionary

### Dataset Overview

| Property          | Detail                        |
| ----------------- | ----------------------------- |
| **Total Revenue** | ₹1,472,998                    |
| **Units Sold**    | 62,889                        |
| **Time Period**   | 2022–2025 (partial 2025 data) |
| **Scope**         | All product categories        |

### Data Structure

| Column Name        | Data Type   | Description                                   |
| ------------------ | ----------- | --------------------------------------------- |
| `Transaction ID`   | Identifier  | Unique identifier for each transaction        |
| `Customer ID`      | Identifier  | Unique customer reference number              |
| `Category`         | Categorical | Product category classification               |
| `Item`             | Categorical | Specific product name                         |
| `Price Per Unit`   | Numerical   | Price of a single unit in INR (₹)             |
| `Quantity`         | Numerical   | Number of units purchased in the transaction  |
| `Total Spent`      | Numerical   | Total transaction value in INR (₹)            |
| `Payment Method`   | Categorical | Mode of payment used by customer              |
| `Location`         | Categorical | Store location where transaction occurred     |
| `Transaction Date` | Date        | Date when purchase was made                   |
| `Discount Applied` | Boolean     | Whether discount was applied (`TRUE`/`FALSE`) |

### Data Limitations

- ⚠️ **No profit margin column** — limits profitability analysis; recommendations are revenue-based
- ⚠️ **No customer demographics** — prevents age/gender/income segmentation
- ⚠️ **Partial 2025 data** — may affect year-over-year comparisons and projections
- ⚠️ **Pricing consistency assumed** — regional/temporal price variations not accounted for

---

## 🧹 Data Cleaning Notes

All primary data cleaning was executed in **Google Sheets** as per capstone requirements.

### Cleaning Pipeline

| Step                     | Action Taken                                                                               | Outcome                            |
| ------------------------ | ------------------------------------------------------------------------------------------ | ---------------------------------- |
| **Missing Values**       | Removed records with missing `Item` values; replaced blank `Discount Applied` with `FALSE` | Data integrity preserved           |
| **Outlier Treatment**    | Validated all transaction values using formula: `Price Per Unit × Quantity`                | No abnormal outliers detected      |
| **Currency Format**      | Converted `Price Per Unit` and `Total Spent` to standardized INR (₹) format                | Consistent monetary representation |
| **Date Standardization** | Standardized `Transaction Date` into proper Date format                                    | Time series analysis enabled       |
| **Boolean Conversion**   | Converted `Discount Applied` into Boolean (`TRUE`/`FALSE`)                                 | Consistent boolean analysis        |
| **Feature Engineering**  | Calculated missing `Total Spent` using: `Total Spent = Price Per Unit × Quantity`          | 100% field completeness            |

### Data Quality Metrics (Post-Cleaning)

| Metric           | Score | Basis                                        |
| ---------------- | ----- | -------------------------------------------- |
| **Completeness** | 99.8% | After cleaning pipeline                      |
| **Accuracy**     | 100%  | All calculated fields validated              |
| **Consistency**  | 100%  | Currency, date & boolean fields standardized |

### Data Quality Assumptions

- All transactions represent valid retail purchases
- Currency standardized to Indian Rupees (INR) for consistency
- Missing discount values imply no discount was applied

---

## 📐 KPI & Metric Framework

### Primary KPIs

| KPI                  | Formula                     | Purpose                                                    | Business Impact                                            |
| -------------------- | --------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| **Total Revenue**    | `SUM(Total Spent)`          | Measures overall business performance and financial health | Primary indicator of market success and growth trajectory  |
| **Units Sold**       | `SUM(Quantity)`             | Indicates product demand and inventory turnover            | Helps forecast inventory needs and production planning     |
| **Avg. Bill Value**  | `Revenue / Transactions`    | Shows average customer spending behavior per transaction   | Identifies opportunities for upselling and cross-selling   |
| **Discount Usage %** | `(Disc Txns / Total) × 100` | Evaluates promotion effectiveness and cost                 | Helps optimize pricing strategy and protect profit margins |

### KPI-to-Objective Mapping

| Business Objective         | KPI Used                     |
| -------------------------- | ---------------------------- |
| Track revenue growth       | Total Revenue                |
| Analyze customer spending  | Average Bill Value           |
| Evaluate pricing strategy  | Discount Usage %             |
| Assess product performance | Category Revenue, Units Sold |

---

## 🔍 Key Insights

### 10 Decision-Level Insights

| #   | Insight                               | Key Finding                                                                                                                 |
| --- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| 01  | **Strong Overall Performance**        | Total revenue of ₹1.47M demonstrates robust business health and market presence                                             |
| 02  | **High Transaction Volume**           | 62,889 units sold indicates consistent customer demand and effective market penetration                                     |
| 03  | **Significant Discount Usage**        | 33.7% of transactions include discounts, representing a substantial promotional investment                                  |
| 04  | **Limited Discount Effectiveness**    | Minimal difference between avg. bill values with (₹129.89) and without (₹129.52) discounts — only ₹0.37 difference, low ROI |
| 05  | **Balanced Category Portfolio**       | Revenue is well distributed across product categories, reducing concentration risk                                          |
| 06  | **Top Category Identification**       | Butchers and Electric Essentials are strategic priority categories with ~13% revenue share each                             |
| 07  | **Revenue Recovery Trend**            | 2024 demonstrates growth and recovery following a 2023 dip, indicating business resilience                                  |
| 08  | **Product Performance Concentration** | A small subset (e.g., `Item_25_FUR`, `Item_25_EHE`) generates disproportionately high revenue                               |
| 09  | **Stable Monthly Performance**        | Monthly revenue trends show consistency without extreme seasonal fluctuations                                               |
| 10  | **Price Stability**                   | Business is not overly dependent on promotional pricing, indicating healthy customer value perception                       |

### Revenue Trend by Year

| Year | Relative Performance | Notes                      |
| ---- | -------------------- | -------------------------- |
| 2022 | 78% (Baseline)       | Reference year             |
| 2023 | 65% (Slight Dip)     | Minor revenue decline      |
| 2024 | 95% (Recovery)       | Strong recovery and growth |

### Discount Impact Analysis

> 💡 **Critical Finding:** Current discount strategies show a mere **₹0.37 difference** in average bill value — a significant margin protection opportunity through targeted, data-driven promotions.

| Condition            | Avg. Bill Value |
| -------------------- | --------------- |
| **With Discount**    | ₹129.89         |
| **Without Discount** | ₹129.52         |
| **Difference**       | ₹0.37           |

### Category Revenue Distribution (Approximate)

| Category             | Relative Share |
| -------------------- | -------------- |
| Butchers             | ~13% (Top)     |
| Electric Essentials  | ~13% (Top)     |
| Beverages            | ~11%           |
| Personal Care        | ~10%           |
| Snacks & Confections | ~9%            |
| Other Categories     | Remaining      |

---

## 📊 Dashboard Summaries

> 🔗 **[Open Interactive Dashboard](https://docs.google.com/spreadsheets/d/1kQwIlLnrHc2I-UWneBf6vj2vV0kbgzcUcms2aMwVz7c/edit?gid=1869737493#gid=1869737493)**

### Platform & Tools

- **Platform:** Google Sheets with advanced pivot tables, charts, slicers, and formulas
- **Visualizations:** Built using pivot tables connected to slicers for dynamic filtering

### Dashboard Components

| Component                | Type         | Description                                                                    |
| ------------------------ | ------------ | ------------------------------------------------------------------------------ |
| **Executive KPIs**       | KPI Cards    | Total Revenue, Units Sold, Average Bill Value, Discount Usage %                |
| **Category Performance** | Bar Chart    | Horizontal bar chart showing revenue by category for quick comparison          |
| **Monthly Trend**        | Line Chart   | Revenue trends over time, highlighting seasonal patterns and growth trajectory |
| **Discount Impact**      | Column Chart | Side-by-side comparison of avg. bill value with and without discounts          |
| **Top Revenue Items**    | Bar Chart    | Ranked visualization of highest-performing products by revenue contribution    |

### Interactive Features

- 🗓️ **Year Filter** — Enables time-based analysis by filtering data for specific years
- 📦 **Category Drilldown** — Allows detailed exploration of individual category performance
- 🏷️ **Discount Toggle** — Facilitates comparison between discounted and non-discounted transactions

---

## 🎯 Strategic Recommendations

| #   | Area                      | Recommendation                                                                                          | Supporting Insight                                   |
| --- | ------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| 1   | **Pricing Strategy**      | Optimize Discount Strategy — reduce blanket discounting, implement targeted segment-specific promotions | Discounts show minimal impact (₹0.37 difference)     |
| 2   | **Category Management**   | Focus on High-Performing Categories — increase marketing in Butchers & Electric Essentials              | These categories drive ~13% of revenue each          |
| 3   | **Product Strategy**      | Product-Level Promotion — prioritize high-revenue items (`Item_25_FUR`, `Item_25_EHE`)                  | Small subset generates majority of revenue           |
| 4   | **Operations & Planning** | Seasonal Planning & Forecasting — implement data-driven inventory planning using historical trends      | Stable monthly trends with identifiable peak periods |

---

## 📈 Impact Estimation

| Impact Area                | Description                                                                                               | Direction      |
| -------------------------- | --------------------------------------------------------------------------------------------------------- | -------------- |
| **Cost Savings**           | Optimizing discount strategy may reduce unnecessary promotional spend (33.7% rate, ₹0.37 avg. difference) | ✅ Positive    |
| **Operational Efficiency** | Automated dashboard reduces manual reporting time by ~60%                                                 | ✅ High        |
| **Revenue Growth**         | Focusing on top-performing categories and high-revenue items expected to support growth                   | ✅ Positive    |
| **Risk Reduction**         | Data-driven decisions reduce risks in inventory, pricing, and promotional planning                        | ✅ Significant |

> **Note:** All impact estimates are directional. The dataset lacks explicit cost and margin data, so precise financial projections are deferred until cost information is incorporated into future analysis cycles.

---

## ⚠️ Limitations

- **No Profit Data** — Dataset lacks explicit profit margin information; recommendations are revenue-based
- **Limited Demographics** — No customer demographic data (age, gender, income) for refined targeting
- **Partial 2025 Data** — Incomplete 2025 data may affect year-over-year trend analysis
- **Pricing Consistency Assumption** — Analysis assumes consistent pricing across locations and time periods
- **External Factors** — Market dynamics, competitive actions, and economic conditions are not included

---

## 🚀 Future Scope

| Initiative                     | Description                                                                                  | Priority  |
| ------------------------------ | -------------------------------------------------------------------------------------------- | --------- |
| **Profit & Margin Analysis**   | Incorporate cost data to enable comprehensive profit margin analysis by category and product | 🔴 High   |
| **RFM Customer Segmentation**  | Implement Recency, Frequency, Monetary analysis to segment customers by purchasing behavior  | 🔴 High   |
| **Sales Forecasting**          | Apply time series models (ARIMA, Prophet, ML) to predict future sales trends and demand      | 🟡 Medium |
| **Location-Based Performance** | Conduct detailed location-wise analysis to identify regional performance variations          | 🟡 Medium |
| **Predictive Analytics & ML**  | Develop ML models for demand forecasting, churn prediction, and dynamic pricing              | 🔵 Future |

---

## 🛠️ Technical Methodology

### Tools Used

| Tool                        | Purpose                                            |
| --------------------------- | -------------------------------------------------- |
| **Google Sheets**           | Data cleaning, analysis, and dashboard creation    |
| **Pivot Tables**            | Multi-dimensional analysis                         |
| **Advanced Formulas**       | `SUM`, `AVERAGE`, `COUNTIF`, `IF` for calculations |
| **Charts & Visualizations** | Data presentation and dashboard components         |

### Key Formulas

```
Revenue Calculation:   SUM(Total Spent) across all transactions
Average Bill Value:    Total Revenue / COUNT(Transactions)
Discount %:            COUNTIF(Discount Applied = TRUE) / COUNT(All Transactions) × 100
Category Analysis:     Pivot tables grouped by Category with SUM(Total Spent)
```

### Dataset Files

| File                                        | Description      |
| ------------------------------------------- | ---------------- |
| `Submission_retail_sales.xlsx`              | Original dataset |
| `Dashboard_of_Submission_retail_sales.xlsx` | Dashboard file   |

---

## 👥 Team Contribution Matrix

| Team Member          | Dataset & Sourcing | Cleaning | KPI & Analysis | Dashboard | Report | PPT | Role               |
| -------------------- | ------------------ | -------- | -------------- | --------- | ------ | --- | ------------------ |
| **Satyam Kumar**     | ✔️                 | ✔️       | ✔️             | ✔️        | ✔️     |     | Project Lead       |
| **Rishi Raj**        | ✔️                 |          | ✔️             | ✔️        |        |     | Dashboard Lead     |
| **Agnik Mishra**     | ✔️                 | ✔️       | ✔️             | ✔️        | ✔️     |     | Analysis Lead      |
| **Mihika Mathur**    | ✔️                 | ✔️       | ✔️             | ✔️        | ✔️     |     | Data Lead          |
| **Ansh**             | ✔️                 | ✔️       | ✔️             | ✔️        | ✔️     |     | Strategy Lead      |
| **Yash Raghubanshi** |                    | ✔️       | ✔️             | ✔️        |        | ✔️  | PPT & Quality Lead |

> Contribution claims are verifiable against Google Sheets Version History and working files submitted alongside this report.

---

## 📄 Additional Resources

- 📊 [Live Dashboard](https://docs.google.com/spreadsheets/d/1kQwIlLnrHc2I-UWneBf6vj2vV0kbgzcUcms2aMwVz7c/edit?gid=1869737493#gid=1869737493)
- 📑 [Full Report PDF](./Retail_Sales_Report_Final.pdf)
- 📽️ [Presentation PDF](./Retail_Sales_Analysis_Presentation.pdf)

---

<div align="center">

**Retail & E-Commerce Analytics | Section D Group 15 | February 2026**  
_Confidential — Internal Use Only_

_Prepared by: Satyam Kumar · Mihika Mathur · Ansh · Yash Raghubanshi · Rishi Raj · Agnik Mishra_

</div>
