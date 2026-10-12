# SWYNEX-E-COMMERCE-SALES-PROJECT-REPORT
Task-4 :- E-commerce sales project report


A portfolio project report for e-commerce sales analysis, data preparation, and dashboard-style reporting. The project follows a raw-to-clean workbook workflow and uses summary metrics and visualizations to examine sales, profit, orders, customers, products, fulfillment, and geography.

> **Validation note:** The figures and metrics below reflect the supplied project report. The report says dashboard values were transcribed from screenshots, and some category shares are approximate. Recalculate them from the final cleaned workbook before presenting them as verified results.

## Project overview

The analysis combines transaction-level order, customer, product, location, payment, shipping, status, and financial fields. It includes an all-status overview dashboard and several charts specifically described as **delivered orders**. Keep those populations separate when comparing metrics.

### Objectives

- Prepare a consistent analysis dataset from the workbook's raw and clean worksheets.
- Summarize sales, profit, order activity, and customer activity.
- Review monthly trends and category-level performance.
- Examine order status, payment mode, and shipping mode distributions.
- Explore delivered sales by customer and US state.
- Turn chart observations into practical operational and reporting recommendations.

## Dataset fields

The report identifies these fields in the workbook screenshots. Confirm the final workbook's exact headers and definitions before analysis.

| Group | Fields shown |
| --- | --- |
| Orders and dates | Order ID, Order Date, Ship Date, Delivery Days, Month, Quarter, Year |
| Customer and location | Customer ID, Customer Name, State, City, Gender, Age |
| Product details | Product Name, Category, Sub Category, Product ID, Brand, Ratings |
| Fulfillment | Shipping Mode, Payment Mode, Order Status |
| Financial measures | Quantity, Discount %, Unit Price, Cost, Sales, Profit |

## Cleaning and preparation workflow

The report describes a raw worksheet and a cleaned worksheet. Use the following as a reproducible checklist, and document only the checks and transformations actually performed in the final project:

1. Confirm headers, row boundaries, and whether each row represents an order or an order line.
2. Check duplicates and investigate repeated Order IDs before removing records; a single order may have multiple line items.
3. Identify missing values in dates, customer and product fields, quantities, costs, sales, and status, then record the treatment.
4. Standardize text categories, payment and shipping modes, states, and order statuses.
5. Set dates and numeric columns to appropriate data types.
6. Derive Month, Quarter, and Year consistently from the selected date field.
7. Verify the business definitions and calculations for Sales, Profit, and all dashboard KPIs.
8. Check implausible values (such as negative quantities or invalid ratings) and reconcile workbook totals with dashboard figures.
9. Preserve the raw worksheet as an audit reference and use the cleaned data as the analysis source.

## Methodology

- **Summary KPIs:** Aggregate order count, sales, and profit; confirm unique-customer logic and what the average-order metric measures.
- **Time analysis:** Group sales by month and sort months chronologically.
- **Product analysis:** Group delivered-order sales by category.
- **Operations:** Count orders by status, payment mode, and shipping mode.
- **Customer and geography:** Rank customers by delivered sales and aggregate delivered sales by state.
- **Dashboarding:** Present consistent metrics, chart filters, currency units, and date ranges. The report suggests Excel, Python, and Tableau or BI-style visualizations; identify the BI tool actually used in the final implementation.

## Findings and reported metrics

### Overview dashboard

The report transcribes these values from the supplied overview screenshot. They have **not been recalculated from the workbook** in this README.

| Metric | Value shown | Qualification |
| --- | ---: | --- |
| Total Orders | 1,018 | Overview dashboard count |
| Total Sales | 1,301,226.80 | Currency/unit is not specified in the report |
| Total Profit | 419,243.69 | Currency/unit is not specified in the report |
| Total Customers | 1,018 | Confirm whether this is a distinct customer count |
| Average Orders | 1,278.22 | Screenshot label is ambiguous; confirm if this is Average Order Value or another measure |

The overview appears to include all order statuses, while the individual Python charts are titled for delivered orders. Do not compare their totals without aligning filters and date ranges.

### Delivered-order charts and status distribution

- **Monthly sales:** The chart spans January 2024 through June 2026 and shows visible peaks around August 2024 and April 2025, with lower values around October 2024, February 2026, and June 2026. June 2026 may be an incomplete period.
- **Category share:** Home is approximately 18.4%, Grocery 18.3%, Sports 17.8%, Fashion 17.1%, Beauty 17.0%, and Electronics 11.4% of delivered sales in the chart. These are approximate shares transcribed from the report.
- **Order status:** Delivered 271 (26.6%), Pending 262 (25.7%), Returned 243 (23.9%), and Cancelled 242 (23.8%); 1,018 orders total. Pending, returned, and cancelled together account for about 73.4% of the displayed status count.
- **Payment mode:** Wallet 218 (21.4%), COD 213 (20.9%), Credit Card 204 (20.0%), Debit Card 204 (20.0%), and UPI 179 (17.6%).
- **Shipping mode:** Express 347 (34.1%), Standard 342 (33.6%), and Same Day 329 (32.3%).
- **Top delivered-sales customers:** Rahul Ali (C1222) is shown at approximately 11.4%, Omar Nguyen (C4949) at 10.9%, and Valentina Johnson (C7392) at 10.7% in the top-ten chart. These are relative shares within that chart, not necessarily shares of all business sales.
- **State sales:** The map suggests Texas is among the higher-value states, with California also comparatively strong. Validate against state totals rather than color intensity alone.

## Recommendations

1. Review Pending, Returned, and Cancelled orders weekly; identify causes and assign corrective actions.
2. Add an order-status funnel with consistent date and filter context.
3. Compare categories using sales, profit, order count, return rate, and ratings together.
4. Track month-over-month and year-over-year results, and mark incomplete periods.
5. Compare shipping modes by delivery time, delays, ratings, shipping cost, and returns.
6. Segment customers into new, repeat, and high-value groups and monitor retention.
7. Add consistent dashboard filters for Year, Month, Category, State, Payment Mode, Shipping Mode, and Order Status.
8. Define every KPI clearly, distinguishing total orders from unique customers and correcting the ambiguous “Average Orders” label.

## Tools and skills

- **Microsoft Excel:** Workbook raw/clean sheets, column checks, derived fields, and preparation.
- **Python and Pandas:** Data loading, grouping, validation, and chart data preparation.
- **Matplotlib or Plotly:** The report lists these for the monthly, category, status, payment, shipping, and customer charts; confirm which library was used.
- **Tableau / BI-style dashboarding:** The report describes dashboarding as a project tool area. Name the final tool actually implemented.
- **Business analysis:** Interpreting patterns, operational questions, and recommendations.

## Limitations and validation notes

- The report is based on screenshots rather than a direct recalculation from the source workbook; chart percentages may be estimates.
- Overview KPIs and delivered-only charts may use different status filters. Align filter context before reconciling totals.
- “Average Orders” is undefined in the screenshot; verify its formula and rename it accurately.
- The state visualization uses US states and city names; confirm this matches the intended dataset context.
- Confirm dataset provenance and whether customer and transaction values are sample/generated data before presenting them as company results.
- The report does not verify that each cleaning check was completed. Record the actual workflow performed and preserve reproducible calculations.
- Customer names and IDs appear in a chart; consider anonymizing them before public sharing if they are not intended for release.

## Conclusion

The project brings together data preparation, KPI reporting, trend analysis, and operational visualizations. The report suggests variation in monthly sales, a broadly distributed category mix, balanced payment and shipping preferences, and a need to investigate order outcomes. The next step is to validate calculations against the cleaned workbook, define KPI formulas and filters, and monitor delivery outcomes, profitability, and customer retention over time.



The `images/` directory is a **suggested location** for the ten report figures. The PDF was supplied, but separate image files were not. Add the corresponding exported screenshots or chart images to `images/` using the filenames above before expecting these embeds to render on GitHub. The README does not fabricate or include screenshot files.


