# 🎮 Video Game Sales Analysis | Excel & Power BI

**Turning 16,000+ rows of raw sales data into a dashboard that tells you exactly who's winning the console wars — and why.**

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

---

## 📌 Overview

This project analyzes a global video game sales dataset spanning **over 16,500 titles** (11,492 after cleaning) released between 1980 and 2016, across every major platform, genre, and publisher. Using **Excel** for data cleaning and feature engineering and **Power BI** for interactive visualization, the project uncovers which publishers, platforms, and genres have historically driven the most global revenue — and how the market has shifted over time.

The end-to-end workflow mirrors a real-world analytics task: raw, messy data → cleaned and enriched dataset → pivoted summaries → interactive dashboard → business insights.

---

## 🎯 Business Questions / Objectives

This analysis was designed to answer:

1. Which **publishers** and **platforms** have generated the most global sales historically?
2. Which **genres** dominate the market, and has that changed over time?
3. How have global sales **trended by release year**, and what does that suggest about the industry's growth cycle?
4. How does **regional performance** (North America, Europe, Japan, Other) compare — and how much of global revenue does NA alone represent?
5. Can games be meaningfully segmented into **performance tiers** (e.g., Blockbuster vs. Niche Title) to simplify reporting for stakeholders?

---

## 🗂️ Repository Structure

```
video-games-sales-analysis/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── VideoGamesSales_RawData.xlsx     # Untouched source data
│   └── cleaned/
│       └── VideoGamesSales_Cleaned.xlsx     # Final cleaned dataset (also used by Power BI)
│
├── excel/
│   └── VideoGamesSales_Analysis.xlsx        # Full workbook: Raw Data | Cleaned Data | PivotTable
│
├── powerbi/
│   ├── VideoGamesSales.pbix                 # Power BI project file
│   └── VideoGamesSales.pbit                 # Power BI template (optional, for reusability)
│
├── images/
│   ├── dashboard-overview.png
│   ├── sales-by-publisher.png
│   ├── sales-by-platform.png
│   └── sales-by-genre.png
│
└── docs/
    └── data-dictionary.md                   # Column definitions (optional but adds polish)
```

> 💡 **Why this structure?** Separating `data/`, `excel/`, `powerbi/`, and `images/` shows recruiters you think about project organization the way a professional analytics team would — not just "everything dumped in one folder."

---

## 🧹 Data Cleaning & Transformation (Excel)

The workbook is organized into **three purpose-built sheets**, following analyst best practice of never modifying raw data directly:

| Sheet | Purpose |
|---|---|
| **Raw Data** | Original, unmodified dataset (16,598 rows) — kept as a permanent source of truth |
| **Cleaned Data** | Cleaned, standardized, and enriched dataset (11,492 rows after removing incomplete records) |
| **PivotTable** | Summarized views used to feed KPIs and cross-check the Power BI dashboard |

### Key cleaning & transformation steps:

- **Text standardization** — Used `PROPER()` and `TRIM()` to fix inconsistent capitalization and stray whitespace in game titles, creating a clean `Cleaned_Game_Name` column.
- **Missing value handling** — Identified and removed records with missing `Year` or `Publisher` values (`N/A` entries) to ensure aggregation accuracy.
- **Feature engineering with `IF` / `IFS`**:
  - `Game_Age_Category` — classifies each title by release era (e.g., *Legacy Title* vs. more recent releases) based on `Year`.
  - `Global_Sales_Category` — segments titles into performance tiers (e.g., *Blockbuster*, *Major Hit*, *Niche Title*) based on `Global_Sales` thresholds.
- **Aggregation formulas** — Used `SUMIF` / `COUNTIF` (e.g., `Total_Games_By_Publisher`, `Yearly_NA_Sales`, `Total_EU_NA_Sales`) to build reusable summary metrics directly in the working dataset, without needing a separate calculation layer.
- **Pivot analysis** — Built PivotTables to validate totals by publisher, platform, and genre before connecting the dataset to Power BI, ensuring the dashboard's numbers were accurate from the start.

---

## 📊 Power BI Dashboard

The interactive dashboard connects directly to the cleaned dataset and includes slicers for **Platform** and **Year**, letting users filter every visual in real time.

### KPIs at a glance:
- **Total Global Sales:** 2.81K (millions of units)
- **Average Sales Per Game:** 7.32
- **Total EU + JP Sales:** 1.21K
- **NA Share of Global Sales:** 47.56%

### Visuals included:
- Global sales **by Publisher** (top performers)
- Global sales trend **by Year** (industry growth/decline over time)
- Global sales **by Genre** (market share breakdown)
- Global sales **by Platform** (console performance comparison)

<!-- 📸 SCREENSHOT PLACEHOLDERS — replace with your actual images -->

### 🖼️ Dashboard Preview

![Full Dashboard Overview](images/dashboard-overview.png)
*Full interactive dashboard with KPI cards, slicers, and all four visuals*

| Sales by Publisher | Sales by Platform |
|---|---|
| ![Publisher](images/sales-by-publisher.png) | ![Platform](images/sales-by-platform.png) |

| Sales Trend by Year | Sales by Genre |
|---|---|
| ![Yearly Trend](images/dashboard-overview.png) | ![Genre](images/sales-by-genre.png) |

> 📌 *Tip: Take clean screenshots of each visual individually, plus one full-dashboard shot, and drop them into the `/images` folder using the exact filenames above so they render automatically.*

---

## 💡 Key Insights & Conclusions

> *Fill these in with your own takeaways once you've explored the dashboard — a few sentence starters below to help.*

- **Publisher dominance:** _(e.g., Nintendo leads global sales by a wide margin, driven largely by first-party titles on its own platforms...)_
- **Platform trends:** _(e.g., Wii and DS dominate historical sales, reflecting Nintendo's casual-market strategy in the mid-2000s...)_
- **Genre performance:** _(e.g., Action and Sports genres together account for over half of global sales...)_
- **Market lifecycle:** _(e.g., Global sales peaked between 2008–2010, coinciding with the 7th console generation, before declining as digital distribution changed the market...)_
- **Regional insight:** _(e.g., North America alone accounts for nearly half of all global sales, making it the most critical region for publisher strategy...)_

---

## 🛠️ Tools & Skills Demonstrated

`Excel` `Power BI` `Data Cleaning` `PROPER/TRIM` `IF/IFS Logic` `SUMIF/COUNTIF` `PivotTables` `Data Modeling` `DAX-ready Data Prep` `Dashboard Design` `Data Storytelling`

---

## 📬 Contact

**[Your Name]**
[LinkedIn](#) • [Portfolio](#) • [Email](#)

---
*If you found this project useful or interesting, consider giving the repo a ⭐ — it helps a lot!*
