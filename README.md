# PeakSport_Retail_Analysis
An entirely Excel based data analysis project that started with a business task for a retail enterprise. The executive summary consists of overall sales, products, customers, inventory and promotions.

**Excel portfolio case study | Data cleaning · KPI development · PivotTables · Business insights**

PeakSport Retail is a fictional sporting-goods retailer used for this portfolio exercise. The workbook contains a synthetic multi-table retail dataset and an Excel-only analysis of sales, profitability, stores, products, promotions, customers, returns, and inventory risk. No real retailer or customer information is used.

> **Workbook:**  [PeakSport_Retail_Excel_Project.xlsx](https://github.com/EnzoMendoza/PeakSport_Retail_Analysis/blob/92973d5df37a3e0139d5f92620f9236c68b8863a/PeakSport_Retail_Excel_Project.xlsx)
> **Dashboard** [[PeakSport_Retail_Excel_Project.pdf]](https://github.com/EnzoMendoza/PeakSport_Retail_Analysis/blob/e828f7d3fca50786453fb30589f82e10782f87ac/PeakSport_Retail_Excel_Project.pdf)
> **Period covered:** January 2025–September 2026  

## Business question

Management needs a data-backed view of performance before the next buying cycle. The analysis is designed to answer:

- How are sales and gross profit changing month over month?
- Which stores and product categories generate sales and profit, and which deserve attention?
- Which products lead or lag in adjusted sales?
- Are promotions associated with strong sales but weak margins?
- How do customer segments differ in order value, frequency, and revenue?
- Which store-product inventory combinations may need replenishment or review for excess stock?

## Headline KPIs

| KPI | Result | Definition |
|---|---:|---|
| Adjusted sales | **$612,515.45** | Net sales less recorded return amount |
| Gross profit after returns | **$261,009.32** | Adjusted sales less adjusted COGS |
| Gross margin after returns | **42.61%** | Total adjusted gross profit ÷ total adjusted sales |
| Distinct orders | **5,200** | Unique OrderIDs |
| Original units sold | **8,276** | Sum of UnitsSold before subtracting returns |
| Units returned | **349** | Sum of ReturnUnits |
| Unit return rate | **4.22%** | Units returned ÷ original units sold |
| Average order value (AOV) | **$117.79** | Adjusted sales ÷ distinct orders |
| Net units retained | **7,927** | Original units sold less returned units |

The workbook's dashboard currently labels 7,927 as “Units Sold.” That is **net units retained**, not original units sold. See the final-review checklist before publishing the workbook as a finished portfolio artifact.

## Dataset at a glance

| Table | Approx. records | Purpose |
|---|---:|---|
| Sales_Raw | 7,576 line items | Transaction-level sales and returns |
| Products | 171 | Product attributes, category, brand, list price, and unit cost |
| Stores | 15 | Store names and location/format attributes |
| Customers | 2,000 | Customer master and segment labels |
| Promotions | 12 | Promotion dates, discount and scope |
| Inventory | 2,565 | Store-product inventory snapshot and derived risk fields |

One order can contain multiple sales line items, so line-item count and distinct order count are not interchangeable.

## Key findings from the workbook

1. **Overall performance:** The analysis reports **$612.5K** in adjusted sales and **$261.0K** in gross profit after returns, for a **42.61%** gross margin.
2. **Category trade-off:** Equipment is the largest category by adjusted sales at **$242,525.45**, while Apparel has the highest calculated category margin at **44.10%**. Equipment's margin is **41.14%**, so the highest-sales category is not the highest-margin category.
3. **Store profitability:** Dallas NorthPark leads store adjusted sales at **$57,594.75**, but its calculated gross margin is **41.82%**, the lowest store margin in the current store analysis. Austin Domain has the lowest adjusted sales at **$27,595.55**.
4. **Customer value:** Loyal customers have the highest revenue per purchasing customer (**$379.47**) and highest orders per customer (**2.95**). VIP customers have the highest AOV (**$133.85**), illustrating that a higher average order does not automatically mean the highest cumulative customer value.
5. Promotion trade-off:** PROMO10 has **$11,354.00** in adjusted sales and a **20.56%** margin; PROMO09 has a **42.32%** margin on **$1,530.00** in adjusted sales. These are descriptive comparisons, not proof that the promotion caused the results.

## Recommendations

1. **Investigate Dallas NorthPark's margin performance.**
  Review product mix, promotional discounts, and cost drivers to identify opportunities to improve profitability without unnecessarily sacrificing sales.

2. **Investigate Austin Domain's sales and returns.** 
  Review the products most frequently returned, customer feedback, and inventory availability. Develop a targeted improvement plan and monitor sales and return rates monthly.

3. **Strengthen customer retention.**
  Investigate how can we convert more Core and Value shoppers into Loyal and VIPs, as the latter average more per order and generate more revenue per customer.

## Excel techniques demonstrated

- Data profiling and a documented cleaning log
- Excel Tables and lookup formulas to connect sales to product, store, and customer reference data
- `SUMIFS`, `COUNTIFS`, `COUNTIF`, `IF`, `VLOOKUP`, `XLOOKUP`, `INDEX`/`MATCH`, and date/text functions
- Calculated fields for adjusted sales, returned COGS, adjusted COGS, gross profit, margin, AOV, return rate, and inventory coverage
- PivotTables and charts for monthly trends, store rankings, product/category performance, promotions, customer segments, and inventory risk
- A management-facing dashboard with KPI cards, findings, and recommendations

The business analysis is Excel-based; no SQL is used in this project.

## Workbook guide

| Worksheet | Contents |
|---|---|
| `Manager Brief` | Business context, questions, and expected deliverables |
| `Sales_Raw` | Original sales source data; preserve as the raw source |
| `Cleaning Log` | Data-quality checks, actions, and validation notes |
| `Products`, `Stores`, `Customers`, `Promotions` | Reference/master tables |
| `Inventory` | Inventory snapshot plus coverage and risk fields |
| `Data Dictionary` | Descriptions for core fields |
| `Sales_Raw Clean` | Working cleaned sales data and derived fields |
| `Sales_Customer Analysis` | Customer-enriched working data for segment analysis |
| `PVT-Trends` | Monthly trend analysis |
| `PVT-Stores` | Store rankings and margin calculations |
| `PVT-Products` | Category/subcategory sales and product rankings |
| `PVT-Inventory` | Reorder and potential-overstock analysis |
| `PVT-Promotions` | Promotion-level sales, profit, margin, and return rate |
| `PVT-Customers` | Customer segment sales, orders, AOV, and revenue per customer |
| `Analysis Template` | KPI summary and section checklist |
| `Dashboard` | Executive-facing KPI cards and charts |

