# Data Dictionary

Reference for columns in `data/processed/Echo Attire Cleaned Pivot Dashboard.xlsx`
(sheet **"Echo Attire"**). The raw file in `data/raw/` has the same fields except
**Age Bracket** and **Months**, which were engineered during cleaning.

| Column | Type | Description |
|---|---|---|
| `index` | Integer | Row identifier / sequence number. |
| `Order ID` | Text | Unique order identifier. |
| `Cust ID` | Integer | Unique customer identifier. |
| `Gender` | Text | Customer gender (`Men` / `Women`). |
| `Age` | Integer | Customer age at time of order. |
| `Age Bracket` | Text | Derived segment: `Teenager`, `Adult`, `Senior`. |
| `Date` | Date | Order date. |
| `Months` | Text | Month name derived from `Date` (used for time-series grouping). |
| `Status` | Text | Order fulfillment status: `Delivered`, `Cancelled`, `Returned`, `Refunded`. |
| `Channel` | Text | Sales/marketplace channel the order was placed through: `Amazon`, `Myntra`, `Flipkart`, `Ajio`, `Nalli`, `Meesho`, or `Others`. Standardized to match the original dataset's marketplace naming for consistency with the PivotTables and dashboard. |
| `SKU` | Text | Stock keeping unit / product code. |
| `Category` | Text | Product category (e.g., Kurta, Saree, Set, Blouse, Bottom, Ethnic Dress, Top, Western Dress). |
| `Size` | Text | Product size (e.g., S, M, L, XL, XXL). |
| `Qty` | Integer | Quantity ordered. |
| `currency` | Text | Transaction currency (INR). |
| `Amount` | Numeric | Order value in local currency. |
| `ship-city` | Text | Shipping destination city. |
| `ship-state` | Text | Shipping destination state. |
| `ship-postal-code` | Text/Integer | Shipping postal code. |
| `ship-country` | Text | Shipping destination country. |
| `B2B` | Boolean | Whether the order was a business-to-business transaction. |

## Notes

- All monetary values are in **INR (₹)**.
- Dataset covers orders placed between **January 2022 and December 2022**.
- `Order ID` is expected to be unique per row; duplicates were removed during cleaning.
