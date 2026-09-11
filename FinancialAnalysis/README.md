# Financial Analysis

A financial dashboard for a SaaS company covering P&L, cash flow, and unit economics.

# Screenshots

![P&L](Screenshots/P_and_L.png)
![Cash Flow](Screenshots/CashLiquidity.png)
![Unit Economics](Screenshots/UnitEconomics.png)

# Report Structure

The report has 3 pages:
**P&L**: Waterfall chart (bridge from revenue to EBIT), combo chart for financial performance, KPI cards with month-over-month trend arrows, pivot table by P&L line, slicers for period and section
**Cash_Flow**: KPI cards, sunburst chart of top 10 cash flow by account, area chart of cumulative cash flow, pivot table reconciling EBIT to operating cash flow
**Unit_Economics**: Bar charts for ROMI, CAC, and LTV, scatter chart of customer tenure vs. MRR by channel, line chart of LTV trend by cohort, KPI cards, slicers by channel and period

## Data Model

A star schema:
**Fact_GL_Transactions** general ledger transactions (P&L)
**Fact_Cash_Payments** cash payments, accrual and cash basis
**Fact_CapEx_Register** capital expenditure register
**Fact_Marketing_Spend** marketing spend by channel
**Fact_Subscription_Monthly** monthly customer subscriptions (MRR, status)
**Dim_Account** chart of accounts with P&L grouping
**Dim_Customer** customer plan, signup/churn date, cohort, tenure
**Dim_Channel** customer acquisition channel
**Dim_Date** calendar
**Assumptions** initial funding amount
**_Measures** a separate table for DAX measures

# Key DAX Measures
- Total_Revenue, Total_COGS, Total_OpEx, Total_DA, Gross_Profit, EBITDA, EBIT
- Operating_Cash_Flow, Investing_Cash_Flow, Net_Cash_Flow, Cumulative_Cash_Flow, Change_in_Working_Capital
- CAC, LTV, LTV_CAC_ratio, Retention_Rate, ROMI, Payback_Period_Months, Cohort_Revenue
- MoM change and arrow measures for trend indicators (e.g. Total_Revenue_MoM_Change, Arrow_Total_Revenue)

# How to Open
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (it's free).
2. Download the file FinancialAnalysis.pbix from this repository.
3. Open the file in Power BI Desktop.
