
# Apparel Sales Analysis - Q4 (2025)

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C8CBF?style=flat-square)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Preprocessing-F7931E?style=flat-square&logo=scikit-learn)

##  Overview

This project analyzes the quarterly sales performance of an Australian apparel company for **Q4 2025**. Using Python, the analysis covers data wrangling, descriptive statistics, temporal trend reporting (daily, weekly, monthly, quarterly), and demographic segmentation across states and consumer groups.

The goal is to surface actionable insights for Sales & Marketing (S&M) teams — identifying peak sales periods, top-performing states, high-value consumer groups, and opportunities for targeted strategies like hyper-personalization and Next Best Offers.

---

##  Dataset

**File:** `Aus_Apparal_Sales_Q4_2025.csv`

The dataset captures transactional sales data for Q4 2025 across Australian states, with the following key attributes:

| Column | Description |
|---|---|
| `Date` | Transaction date |
| `Time` | Time of day (Morning / Afternoon / Evening) |
| `State` | Australian state (VIC, NSW, WA, etc.) |
| `Group` | Consumer demographic (Kids, Women, Men, Seniors) |
| `Sales` | Revenue from the transaction |
| `Unit` | Units sold |

---

##  Tools & Libraries

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, grouping, and reporting |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical and business visualizations |
| `sklearn.preprocessing` | MinMax normalization of Sales and Unit columns |
| `datetime` | Date/time parsing and period extraction |

> **Recommended visualization package:** Seaborn — chosen for its clean statistical plots, built-in themes, and minimal code overhead, making it well-suited for business dashboards.

---

##  Project Workflow

### 1. Data Wrangling
- Inspected dataset shape and column info
- Identified and handled missing values — rows with all-null entries dropped; remaining `Sales` nulls filled with column mean
- Applied **MinMax normalization** to `Sales` and `Unit` columns to ensure fair feature weighting
- Generated state-wise sales overview via grouped aggregation

### 2. Data Analysis
- Computed descriptive statistics (mean, std, min, max, mode) for `Sales` and `Unit`
- Identified the **highest** and **lowest** performing consumer groups
- Extracted temporal features (`week`, `month`, `quarter`) from the `Date` column
- Generated **weekly**, **monthly**, and **quarterly** sales rollup reports

### 3. Data Visualisation
- **State-wise sales by consumer group** — grouped bar chart (hue: Group)
- **Group-wise sales by state** — grouped bar chart (hue: State)
- **Time-of-day sales analysis** — boxplot identifying peak vs. off-peak periods
- **Daily sales trend** — line plot with markers across Q4
- **Weekly sales trend** — line plot with markers by ISO week
- **Monthly sales trend** — bar chart by month
- **Quarterly sales trend** — bar chart by quarter

### 4. Report Generation
- Auto-generated a structured text report summarizing:
  - Top and lowest performing states
  - Highest and lowest sales demographic groups
  - Daily, weekly, monthly, and quarterly trend observations
  - Strategic recommendations for inventory, marketing, and promotions

---

##  Key Findings

| Metric | Result |
|---|---|
| Top performing state | VIC |
| Lowest performing state | WA |
| Highest sales group | Men |
| Lowest sales group | Seniors |

---

##  Repository Structure

```
apparel-sales-analysis/
│
├── Sales_Project_Analysis.ipynb       # Main analysis notebook
├── Aus_Apparal_Sales_Q4_2025.csv      # Dataset
└── README.md                          # Project documentation
```

---

##  Business Recommendations

- **Optimize inventory** for identified peak hours (time-of-day analysis)
- **Improve marketing strategies** in low-performing states like WA
- **Target Men and Women segments** for high-ROI campaigns
- **Leverage Q4 trends** for future promotional planning and demand forecasting

---

##  Author

**Abhinav Srivastava**  
Last Updated: 31 May 2026

