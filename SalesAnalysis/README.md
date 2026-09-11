# Sales Analysis

A sales dashboard for a retail company covering revenue, profit, product categories, stores, and customer segments. 

# Screenshots

![Executive](Screenshots/executive.png)
![Product](Screenshots/product.png)
![Store](Screenshots/store.png)
![Customer](Screenshots/customer.png)

# Report Structure

The report has 4 pages:
**Executive**: KPI cards (profit, margin, year growth, average order value), combo chart for sales and margin, treemap by region, decomposition tree
**Product**: Pivot table, combo charts for margin/sales by product, scatter chart of sales vs. margin vs. revenue per customer, by category
**Store**: Top 5 stores by sales, a table with key numbers, a map of profit by region 
**Customer**:  Number of customers, average revenue per customer, repeat purchase rate, age and segment distribution, map of cost by country 

## Data Model

A simple star schema:
**Fact_Sales_Transactions** sales transactions
**Dim_Customers** segment of customers, age group, country
**Dim_Products** category of products, subcategory, product name
**Dim_Stores** store region, country, store name
**Dim_Calendar** calendar
**_Measures** a separate table for DAX measures

# Key DAX Measures
- TotalSales, TotalCost, TotalProfit, ProfitMargin
- TotalQty, AvgOrderValue, SalesPerStore, StoreRank
- YearGrowth
- CustomerCount, AvgRevPerCust, AvgCustAge, Repeat Purchase Rate

# How to Open
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (it's free).
2. Download the file SalesAnalisys_port.pbix from this repository.
3. Open the file in Power BI Desktop.