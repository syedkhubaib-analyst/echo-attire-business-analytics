# Echo Attire: Sales Performance Analysis & Dashboard

An end-to-end Data Analytics & Business Analytics project on a year of e-commerce sales
data for **Echo Attire**, an apparel retailer selling across multiple online marketplaces.
The project covers data cleaning, pivot-table analysis, and an interactive Excel
dashboard that surfaces revenue trends, customer demographics, order fulfillment health,
and channel performance.

![Echo Attire Sales Dashboard](images/Echo%20Attire%20Sales%20Dashboard.jpg)

---

## 📌 Project Overview

- **Business objective:** Echo Attire wants an annual sales report for 2022 so the business
can understand its customers and grow sales in 2023. This project answers that brief end
to end from raw data, to a clean model, to a dashboard, to a concrete, data-backed
recommendation for where to focus 2023 marketing spend.

<table>
  <tr><td><b>Domain</b></td><td>E-commerce / Retail (Apparel)</td></tr>
  <tr><td><b>Tool used</b></td><td>Microsoft Excel (Power Query, PivotTables, PivotCharts, Slicers)</td></tr>
  <tr><td><b>Dataset size</b></td><td>31,047 orders</td></tr>
  <tr><td><b>Time period</b></td><td>January 2022 – December 2022</td></tr>
  <tr><td><b>Currency</b></td><td>INR (₹)</td></tr>
  <tr><td><b>Type</b></td><td>Descriptive analytics / BI dashboard</td></tr>
</table>

---

## 🗂️ Repository Structure

```
echo-attire-business-analytics/
├── README.md                                  <- You are here
├── data/
│   ├── raw/
│   │   └── Echo Attire Dataset.xlsx           <- Original, unmodified source data
│   └── processed/
│       └── Echo Attire Cleaned Pivot Dashboard.xlsx   <- Cleaned data + PivotTables + Dashboard
│                                                      (sheets: "Echo Attire", "Pivot Table", "Dashboard")
├── docs/
│    ├── Business Requirements.md                <- Business objective, questions, and deliverable mapping
│    ├── Data Dictionary.md                      <- Column-by-column field reference 
│    └── Insights & Recommendations.md           <- Verified insights + final growth recommendations
│                                                                                             
└── images/
    └── Echo Attire Sales Dashboard.jpg        <- Dashboard preview image
```

---

## 🧹 Data Cleaning & Preparation

Starting from the raw export (`data/raw/Echo Attire Dataset.xlsx`), the following steps
were applied to produce the analysis-ready table in
`data/processed/Echo Attire Cleaned Pivot Dashboard.xlsx` (sheet **"Echo Attire"**):

- Removed duplicate and blank rows.
- Standardized text fields (category names, state names, casing/spacing).
- Converted `Date` to a proper date type and derived a **`Months`** helper column for
  time-series grouping.
- Derived an **`Age Bracket`** column (Teenager / Adult / Senior) from raw `Age` to
  support demographic segmentation.
- Validated categorical fields (`Status`, `Channel`, `Gender`, `Category`, `Size`) against
  a fixed set of expected values.
- Standardized `Channel` values to the marketplace names used in the original dataset
  (Amazon, Myntra, Flipkart, Ajio, Nalli, Meesho, Others) so the raw data, cleaned data,
  PivotTables, and dashboard all reference a consistent channel taxonomy.
- Checked `Amount` for negative/zero/outlier values.

The cleaned table feeds the **"Pivot Table"** sheet, which contains all the aggregations
behind the dashboard (monthly sales & order count, gender split, order status split,
top states, channel mix, and age-bracket × gender order share). The **"Dashboard"** sheet
assembles these pivots into the final report shown above.

---

## 📊 Dashboard Highlights

**Key metrics (FY2022):**

| Metric | Value |
|---|---|
| Total orders | 31,047 |
| Total revenue | ₹21,176,377 |
| Average order value | ₹682 |
| Delivered rate | 92.3% |
| Cancelled / Returned / Refunded | 2.7% / 3.4% / 1.7% |

**What the dashboard shows:**

- **Orders & Sales (monthly trend):** combo chart tracking revenue and order volume
  from January to December, highlighting a Q1 peak (March) and a gradual decline into
  Q4.
- **Male & Female Sales Ratio:** women account for ~64% of revenue vs. ~36% for men.
- **Order Status:** 92% of orders are delivered successfully; cancellations, returns,
  and refunds together make up under 8%.
- **Sales by Channel:** marketplace mix led by Amazon (~35.5%), followed by Myntra
  (~23.3%) and Flipkart (~21.6%), with Ajio, Nalli, Meesho, and Others making up the rest.
- **Top 5 States by Sales:** Maharashtra, Karnataka, Uttar Pradesh, Telangana, and
  Tamil Nadu are the highest-revenue states (full top 10 in
  `docs/Insights & Recommendations.md`).
- **Orders by Gender & Age Bracket:** Adult women are the single largest segment
  (34.6% of all orders), followed by teenage women; male segments trail across all age
  brackets.
- **Highest-selling category:** "Set" alone drives 49.6% of revenue, followed by Kurta
  at 23.4% (see `docs/Insights & Recommendations.md` for the full category breakdown).
- Fully interactive via **slicers** for Month, Category, and Channel.

---

## 🎯 Business Questions Answered

This project was built to answer Echo Attire's specific 2022 annual-report questions
sales & orders trend, best month, gender split, order statuses, top states, age/gender
relationship, channel performance, and category performance. See
**[`docs/Business Requirements.md`](docs/Business%20Requirements.md)** for the full
question-to-deliverable mapping.

## 💡 Verified Insights & Final Recommendation

Every insight below was independently recalculated from the cleaned dataset (not just
read off the dashboard), see **[`docs/Insights & Recommendations.md`](docs/Insights%20%26%20Recommendations.md)**
for the full breakdown, verification table, and supporting recommendations.

- Women drive **64.1%** of revenue vs. 35.9% for men.
- **Maharashtra → Karnataka → Uttar Pradesh** are confirmed as the top 3 states by sales.
- The **30–49 age group contributes ~50.1%** of both orders and revenue.
- **Amazon, Myntra, and Flipkart** together drive **80.4%** of total revenue.

**Final recommendation:** Target women customers aged 30–49 in Maharashtra, Karnataka,
and Uttar Pradesh with ads, offers, and coupons on Amazon, Myntra, and Flipkart, this
segment sits at the intersection of the highest-value customer dimensions and the
highest-value sales channels, making it the highest-leverage group for 2023 marketing
spend.

---

## 🛠️ How to Use This Project

1. Clone or download the repository.
2. Open `data/processed/Echo Attire Cleaned Pivot Dashboard.xlsx` in Excel.
3. Explore:
   - **"Echo Attire"** sheet → cleaned, tabular source data.
   - **"Pivot Table"** sheet → underlying PivotTables for every chart.
   - **"Dashboard"** sheet → the interactive report (use the slicers to filter by
     Month / Category / Channel).
4. Reference `docs/Data Dictionary.md` for column definitions if you extend the analysis.
5. The original, untouched export is preserved in `data/raw/` for reproducibility,
   any cleaning step can be re-run or audited against it.

---

## 💡 Skills Demonstrated

- Data cleaning & preparation (Power Query / manual transforms)
- Feature engineering (Age Bracket, Month extraction)
- PivotTables & PivotCharts
- KPI design and dashboard storytelling
- Slicer-based interactivity for self-service filtering
- Business insight generation from transactional retail data

---

## 🙋 About

Built as a Data Analyst, Business Analyst project to demonstrate the full
workflow from raw data to a decision-ready dashboard.
