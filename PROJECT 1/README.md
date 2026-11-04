<div align="center">

# -- ! Superstore Sales Dashboard ! --
### *An Interactive Power BI Report for Sales, Profit & Product Performance Analysis of a Retail Superstore*

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures-0078D4?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Modeling-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![Data Visualization](https://img.shields.io/badge/Data-Visualization-A62817?style=for-the-badge)](https://powerbi.microsoft.com/)

<br/>

> *"Numbers alone are noise — a good dashboard turns them into decisions."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧬 Data Model](#-data-model)
- [📈 KPI Cards](#-kpi-cards)
- [🎛️ Interactive Filters](#️-interactive-filters)
- [🧩 Report Pages](#-report-pages)
- [📊 Sample Output](#-sample-output)
- [🖼️ Screenshots](#️-screenshots)
- [🛠️ Tech Stack](#️-tech-stack)
- [🏆 Advantages](#-advantages)
- [🔑 Key Insights](#-key-insights)
- [🚀 How to Use](#-how-to-use)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Superstore Sales Dashboard** is an interactive **Power BI** report built on the Superstore retail dataset. It brings sales, profit, quantity and discount data together on a single page, and lets the user slice the numbers by **Region** and **Category** with one click — no formulas or extra queries required.

The report contains **two pages**: a high-level **Sales Dashboard** with KPI cards and charts, and a detailed **Order Details** table for drilling down to individual order lines.

This project is designed to:
- Demonstrate a practical **business intelligence workflow**: load → model → measure → visualize → interpret
- Summarize business health through **four headline KPIs** (Total Sales, Total Profit, Total Quantity, Average Discount)
- Compare performance across **categories, regions and sub-categories** using clustered bar charts
- Provide **interactive slicers** so that every visual updates together
- Offer a transaction-level **Order Details** view for auditing and drill-down

---

## 🎯 Problem Statement

> **Objective:** Design and develop an interactive Power BI dashboard that analyzes Superstore sales data and answers key business questions — *How much are we selling? Where are we profitable? Which products drive revenue?*

The dashboard must show overall KPIs, break performance down by category, region and sub-category, allow filtering, and expose the underlying order-level records.

| 📂 Module | 📄 Type | 🔍 Description |
|-----------|---------|----------------|
| KPI Cards | Summary | Total Sales, Total Profit, Total Quantity, Average Discount |
| Sales by Category | Bar Chart | Sales comparison across Technology, Furniture and Office Supplies |
| Profit by Region | Bar Chart | Profit comparison across West, East, South and Central |
| Top 5 Sub Categories | Bar Chart | Five best-selling sub-categories by sales amount |
| Slicers | Filter | Region and Category dropdown filters |
| Order Details | Table | Line-level order records with totals |

The goal is to demonstrate **practical use of Power BI** — data modeling, aggregation, visual design and interactivity — through one clean, easy-to-read report.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📊 **4 KPI Cards** | Total Sales, Total Profit, Total Quantity and Average Discount at a glance |
| 🗂️ **Sales by Category** | Horizontal bar chart comparing sales of each product category |
| 🌍 **Profit by Region** | Compares profit amount across the four sales regions |
| 🏅 **Top 5 Sub Categories** | Ranks the best-performing sub-categories by sales |
| 🎛️ **Region Slicer** | Dropdown to filter the whole dashboard by region |
| 🎛️ **Category Slicer** | Dropdown to filter the whole dashboard by category |
| 📋 **Order Details Page** | Table of order code, year, number, date, customer, region, category, product, quantity, sales and profit |
| ➕ **Grand Totals** | Total row at the bottom of the Order Details table |
| 🎨 **Consistent Theme** | Red & charcoal colour palette for a clean, professional look |
| 🖱️ **Cross-Filtering** | Clicking a bar or slicer value updates every related visual |

---

## 🏗️ Project Structure

```
📦 superstore-sales-dashboard/
│
├── 📄 Aastha_Superstore_PR1.pbix   ← Power BI report file (data model + 2 report pages)
├── 🖼️ screenshots/
│   ├── SALES_DASHBOARD.png          ← Dashboard page screenshot
│   └── ORDER_DETAILS.png            ← Order Details page screenshot
│
└── 📄 README.md                     ← Project documentation
```

---

## 🔄 Project Workflow

```
Project Start
      │
      ▼
┌─────────────────────────────┐
│   Import Superstore Data    │  ← Load the dataset into Power BI
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Clean & Model Data        │  ← Power Query: types, columns, formats
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Create Measures           │  ← Sales, Profit, Quantity, Average Discount
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Design Visuals            │  ← KPI cards, bar charts, table, slicers
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Add Interactivity         │  ← Region & Category slicers, cross-filtering
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Analyze & Interpret       │  ← Read insights from the final dashboard
└────────────┬────────────────┘
             │
             ▼
      Publish / Share Report ✅
```

---

## 🧬 Data Model

The report is built on a single table named **`Superstore`**. Every visual in the report reads its fields from this table.

| Field | Type | Used In |
|-------|------|---------|
| `Order Code` | Text | Order Details table |
| `Order Year` | Whole number | Order Details table |
| `Order Number` | Text / Number | Order Details table |
| `Order Date` | Date (`dd/mm/yyyy`) | Order Details table |
| `Customer Name` | Text | Order Details table |
| `Region` | Text | Region slicer, Profit by Region, Order Details |
| `Category` | Text | Category slicer, Sales by Category, Order Details |
| `Sub Category` | Text | Top 5 Sub Categories chart |
| `Product Name` | Text | Order Details table |
| `Quantity` | Whole number | Total Quantity KPI, Order Details |
| `Sales Amount` | Decimal | Total Sales KPI, all sales charts |
| `Profit Amount` | Decimal | Total Profit KPI, Profit by Region |
| `Discount` | Decimal (%) | Average Discount KPI |

**Key Concepts Used:**

| Concept | Detail |
|---------|--------|
| Aggregation | `SUM` for sales, profit and quantity; `AVERAGE` for discount |
| Cross-Filtering | Slicers and charts filter each other automatically |
| Conditional Layout | Cards, charts and slicers aligned on a 1920 × 1080 canvas |
| Multi-Page Report | Summary dashboard + detailed drill-down table |

---

## 📈 KPI Cards

> The top row of the dashboard shows four headline numbers that update with the slicers.

| KPI | Aggregation | Value on Dashboard |
|-----|-------------|--------------------|
| 💰 **Total Sales** | Sum of `Sales Amount` | **1.50M** |
| 📈 **Total Profit** | Sum of `Profit Amount` | **178.57K** |
| 📦 **Total Quantity** | Sum of `Quantity` | **25K** |
| 🏷️ **Average Discount** | Average of `Discount` | **15.70%** |

---

## 🎛️ Interactive Filters

| Slicer | Field | Behavior |
|--------|-------|----------|
| 🌍 **Region** | `Superstore[Region]` | Dropdown — choose one or more regions (East, West, Central, South) |
| 🗂️ **Category** | `Superstore[Category]` | Dropdown — choose one or more categories (Technology, Furniture, Office Supplies) |

Selecting a value in either slicer instantly refreshes the KPI cards and all three charts.

---

## 🧩 Report Pages

### 📄 Page 1 — Sales Dashboard

| Visual | Type | Fields | Purpose |
|--------|------|--------|---------|
| Total Sales / Profit / Quantity / Avg Discount | Card | Sales Amount, Profit Amount, Quantity, Discount | Headline KPIs |
| **Sales by Category** | Clustered Bar | `Category` × Sum of `Sales Amount` | Compare category revenue |
| **Profit by Region** | Clustered Bar | `Region` × Sum of `Profit Amount` | Find the most / least profitable region |
| **Top 5 Sub Categories by Sales** | Clustered Bar | `Sub Category` × Sum of `Sales Amount` (Top 5) | Identify best-selling sub-categories |
| Region & Category | Slicer | `Region`, `Category` | Filter the full page |

### 📄 Page 2 — Order Details

A detailed table with the following columns:

`Order Code` · `Order Year` · `Order Number` · `Order Date` · `Customer Name` · `Region` · `Category` · `Product Name` · `Sum of Quantity` · `Sum of Sales Amount` · `Sum of Profit Amount`

The table ends with a **Total** row, so the user can verify the numbers behind the dashboard.

---

## 📊 Sample Output

**Sales Dashboard — Chart Values**

| Sales by Category | Sales | | Profit by Region | Profit | | Top 5 Sub Category | Sales |
|---|---|---|---|---|---|---|---|
| Technology | 0.50M | | West | 66K | | Chairs | 0.22M |
| Furniture | 0.50M | | East | 50K | | Phones | 0.21M |
| Office Supplies | 0.49M | | South | 38K | | Storage | 0.15M |
| | | | Central | 25K | | Tables | 0.14M |
| | | | | | | Binders | 0.14M |

**Order Details — Table Totals**

```
Sum of Quantity       : 31,129
Sum of Sales Amount   : 1,867,547.71
Sum of Profit Amount  :   226,098.34
```

**Sample Rows from Order Details**

| Order No. | Date | Customer | Region | Category | Product | Qty | Sales | Profit |
|-----------|------|----------|--------|----------|---------|-----|-------|--------|
| 100006 | 07/09/2014 | Dennis Kane | East | Technology | AT&T EL51110 DECT | 3 | 377.97 | 109.61 |
| 100090 | 08/07/2014 | Ed Braxton | West | Furniture | Hon 2111 Invitation Series Corner Table | 3 | 502.49 | -87.94 |
| 100678 | 18/04/2014 | Kunst Miller | Central | Furniture | DMI Arturo Collection Mission-style Design Wood Chair | 3 | 317.06 | -18.12 |
| 100895 | 02/06/2014 | Stewart Visinsky | South | Office Supplies | Hot File 7-Pocket, Floor Stand | 2 | 356.94 | 107.08 |

---

## 🖼️ Screenshots

**Page 1 — Superstore Sales Dashboard**

![Superstore Sales Dashboard](c:\POWER BI\PROJECT 1\OUTPUT PHOTOS\SALES DASHBOARD.png)

**Page 2 — Order Details**

![Order Details](c:\POWER BI\PROJECT 1\OUTPUT PHOTOS\ORDER DETAILS.png)

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Power BI Desktop** | Latest | Report building, visuals and publishing |
| 🔧 **Power Query** | Built-in | Data loading and cleaning |
| 🧮 **DAX** | Built-in | Aggregations and measures |
| 📁 **Superstore Dataset** | CSV / Excel | Source retail sales data |
| 🎨 **Power BI Theme** | Custom | Red & charcoal colour scheme |

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Beginner Friendly** | Covers the complete Power BI workflow in a simple two-page report |
| 👀 **At-a-Glance Insights** | KPIs and charts answer the main business questions in seconds |
| 🎛️ **Interactive** | Region and Category slicers let users explore without any technical skill |
| 🔍 **Drill-Down Ready** | Order Details page links every KPI back to individual transactions |
| 🔄 **Reusable Template** | Can be reused with any similarly shaped sales dataset |
| 🎨 **Clean Design** | Consistent colours, titles and layout make the report easy to read |
| 📦 **Single Source** | One data table keeps the model simple and fast |

---

## 🔑 Key Insights

- The **West** region is the most profitable at about **66K**, while **Central** is the lowest at about **25K** — West earns more than 2.5× the profit of Central.
- Sales are spread almost evenly across the three categories — **Technology (0.50M)**, **Furniture (0.50M)** and **Office Supplies (0.49M)** — so no single category dominates revenue.
- **Chairs (0.22M)** and **Phones (0.21M)** are the top two sub-categories by sales, followed by Storage, Tables and Binders.
- The top five sub-categories come from all three categories — **Furniture** (Chairs, Tables), **Technology** (Phones) and **Office Supplies** (Storage, Binders) — showing that both big-ticket items and everyday supplies drive revenue.
- The **average discount is 15.70%**, which is significant — discounting should be monitored carefully against profit.
- Some **Furniture** orders show **negative profit** (e.g., Hon 2111 Corner Table, DMI Arturo Chair), which suggests heavy discounting or high costs on certain products.
- The dashboard's headline figures differ from the Order Details totals because the dashboard chart subtitle indicates a **Consumer & Corporate segment** view, whereas the Order Details table shows the full dataset total.
- Overall, the project shows a complete workflow of **data loading → modeling → KPI creation → visualization → business insight**, useful for practical business analysis.

---

## 🚀 How to Use

1. Download or clone this repository.
2. Install **[Power BI Desktop](https://powerbi.microsoft.com/desktop/)** (free, Windows).
3. Open `Aastha_Superstore_PR1.pbix`.
4. Use the **Region** and **Category** slicers on the *Sales Dashboard* page to filter the data.
5. Switch to the *Order Details* page to inspect individual order lines.
6. Click any bar in a chart to cross-filter the other visuals.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Aastha Chodvadiya

[![GitHub](https://img.shields.io/badge/GitHub-yourhandle-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/24se02ml135-boop/python-project)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chodvadiya-aastha-8b79a4418/)

> *"Every dashboard starts with a single question — answer it clearly, and the rest follows."*

**🎓 Role:** Junior Data Analyst | Power BI & Python Enthusiast \
**📍 Location:** India \
**🛠️ Skills:** Power BI · DAX · Power Query · Python · Pandas · Data Analysis · Data Visualization

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📊 [Power BI Official Documentation](https://learn.microsoft.com/en-us/power-bi/) — Report building, visuals and slicers
- 🧮 [DAX Guide](https://dax.guide/) — Measures and aggregation reference
- 🔧 [Power Query Documentation](https://learn.microsoft.com/en-us/power-query/) — Data cleaning and transformation
- 🧠 [GeeksForGeeks — Power BI](https://www.geeksforgeeks.org/power-bi/) — Concept and practice reference
- 💬 [Microsoft Fabric Community](https://community.fabric.microsoft.com/) — Problem-solving support
- 📖 [Kaggle Datasets](https://www.kaggle.com/datasets) — Superstore dataset reference

---

<div align="center">

---

*Made with ❤️ and ☕ — Last updated: November 2026*

</div>
