# Amazon India E-Commerce Sales Dashboard (Excel)

![Dashboard](images/dashboard.png)

An interactive, dark-themed sales dashboard built in Excel on top of a 1,000-order Amazon India dataset (Jan–Dec 2026). It uses Pivot Tables for the analysis layer and formula-driven KPI cards and charts for the dashboard layer, with dropdown filters that update everything at once.

## What's inside

| Sheet | Purpose |
|---|---|
| `dashboard` | The final dashboard: KPI cards, charts, key insights and filters |
| `pivot table` | Pivot Tables and KPI calculations built from the raw data |
| `Amazon_Sales_2026` | Cleaned dataset, stored as an Excel Table (`tblAmazonSales`, 1,000 rows × 44 columns) |
| `Dashboard_Data` | Formula-based data model that feeds the dashboard and responds to the filters |

## Dashboard features

- **6 KPI cards:** Total Sales, Total Profit, Total Orders, Average Order Value, Sales Target (with achievement %), Delivery Rate. Each has a sparkline or progress bar.
- **6 charts:** Monthly sales trend vs target and profit, order status, sales vs target by region, sales by category, payment methods, top 5 brands.
- **Key insights panel:** top region, top category, peak month, top payment method, average delivery time. All update with the filters.
- **3 dropdown filters:** Region, Category, Quarter.
- Region and Category charts ignore their own filter so the comparison stays visible.

## Headline numbers (no filters)

| Metric | Value |
|---|---|
| Net Sales | ₹16.20M |
| Sales Target | ₹16.94M (95.7% achieved) |
| Profit | ₹5.76M (35.5% margin) |
| Orders | 1,000 (67.8% delivered, 15.1% cancelled) |
| Top region | East, ₹4.67M |
| Top category | Fashion, ₹7.21M |
| Peak month | March, ₹2.25M |
| Top payment method | Net Banking, ₹3.47M |

## Data notes

- Net Sales includes cancelled orders (₹1.87M), consistent with the Pivot Tables.
- The `Category` column does not always match the product or SKU prefix. For example, some `ELE-` (electronics) SKUs are labelled Fashion or Grocery, so the Electronics category looks smaller than the brands suggest. The dashboard uses `Category` as provided.
- `fashion` (lowercase) appears in 44 rows. Excel Pivot Tables and formulas treat it the same as `Fashion`.

## How to use

1. Open the file in desktop Excel and go to the `dashboard` sheet.
2. Use the Region, Category and Quarter dropdowns at the top right. Set them back to `All` to reset.
3. If you add rows to `tblAmazonSales`, refresh the Pivot Tables (Data → Refresh All). The dashboard formulas update automatically.

## Tools and skills

- Microsoft Excel: Excel Tables, Pivot Tables, GETPIVOTDATA, SUMIFS/COUNTIFS/AVERAGEIFS, data validation, charts, shape-linked text
- Dashboard design and formula model built with assistance from Claude (Anthropic)

## Requirements

Desktop Excel (Windows). The `.xlsm` file contains no macros. The dashboard uses the Segoe UI font.
