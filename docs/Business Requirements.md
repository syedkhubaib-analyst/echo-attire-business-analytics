# Business Requirements: Echo Attire 2022 Annual Sales Report

## Objective

Echo Attire wants an annual sales report for 2022 so the business can understand its
customers and grow sales in 2023.

## Business Questions & Where They're Answered

Every question below is answered by a specific chart in
`data/processed/Echo Attire Cleaned Pivot Dashboard.xlsx` (sheet **"Dashboard"**), backed
by a PivotTable on the **"Pivot Table"** sheet.

| # | Business Question | Answered By | Dashboard Chart |
|---|---|---|---|
| 1 | Compare sales and orders in a single view | Monthly `Sum of Amount` + `Count of Order ID` combo chart | Orders & Sales |
| 2 | Which month had the highest sales and orders? | Same monthly combo chart | Orders & Sales |
| 3 | Who purchased more — men or women? | Gender split pie chart | Male & Female Sales Ratio |
| 4 | What are the different order statuses? | Status breakdown pie chart | Order Status |
| 5 | Top 10 states contributing to sales | State ranking bar chart (dashboard shows top 5; full top 10 in `docs/Insights & Recommendations.md`) | Top 5 (10) States With Highest Sales |
| 6 | Relationship between age and gender by order volume | Age Bracket × Gender clustered bar chart | Orders Based on Gender & Age Brackets |
| 7 | Which channel contributes the most sales? | Channel-wise sales share pie chart | Sales Based on Different Channels |
| 8 | And more... | Average order value, cancellation/return/refund rate | Order Status, KPI summary in README |

## Deliverable Mapping

| Deliverable | File |
|---|---|
| Raw transactional data | `data/raw/Echo Attire Dataset.xlsx` |
| Cleaned data + PivotTables + Dashboard | `data/processed/Echo Attire Cleaned Pivot Dashboard.xlsx` |
| Dashboard preview | `images/Echo Attire Sales Dashboard.jpg` |
| Field-level documentation | `docs/Data Dictionary.md` |
| Verified insights & business recommendations | `docs/Insights & Recommendations.md` |
| This requirements-to-deliverable mapping | `docs/Business Requirements.md` |

