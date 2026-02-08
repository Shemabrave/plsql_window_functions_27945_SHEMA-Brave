# plsql_window_functions_27945_SHEMA-Brave
# Business Context
A real estate management company operating in the property and housing industry, within the Sales and Property Management department, manages residential and commercial properties across multiple cities and regions
# Data Challenge
The company stores data in separate tables for properties, agents, clients, and sales transactions. Management finds it difficult to evaluate agent performance and property sales trends across regions because meaningful insights require combining multiple tables and comparing results within each region and time period
# Expected Outcome
The analysis is expected to identify the top-selling properties in each region, rank real estate agents based on total sales value, and support strategic decisions on agent incentives and regional investment focus
# 1.Identify Top 5 Properties per Region per Quarter — RANK()
Goal:
Rank properties based on their total sales value within each region and quarter to identify the top 5 best-performing properties

Measurement:

Partition data by region and quarter

Rank properties using total sale price

Select only properties ranked 1 to 5

Business Value:
Helps management focus marketing efforts on high-demand property types and prioritize similar investments in each region

# 2.Calculate Running Monthly Sales Totals — SUM() OVER()

Goal:
Compute cumulative monthly sales revenue for each region to monitor sales momentum over time

Measurement:

Partition by region

Order by month

Calculate running totals of sales value

Business Value:
Allows executives to track growth trends, identify seasonal patterns, and assess whether sales targets are being met progressively

# 3.Analyze Month-over-Month Sales Growth — LAG() / LEAD()

Goal:
Compare each month’s sales revenue with the previous month to determine month-over-month growth or decline.

Measurement:

Retrieve previous month’s sales using LAG()

Calculate percentage or absolute change

Business Value:
Enables early detection of declining markets, supports proactive pricing strategies, and informs management about market performance shifts.

# 4.Segment Clients into Quartiles Based on Purchase Value — NTILE(4)

Goal:
Classify clients into four quartiles based on their total property purchase value, ranging from lowest to highest.

Measurement:

Order clients by total spending

Assign quartiles using NTILE(4)

Business Value:
Supports targeted marketing strategies, loyalty programs, and personalized client engagement based on spending behavior.

# 5.Compute Three-Month Moving Average of Sales — AVG() OVER()

Goal:
Calculate a three-month moving average of sales revenue for each region to smooth short-term fluctuations and reveal long-term trends.

Measurement:

Use a rolling window covering the current month and previous two months

Compute average sales value

Business Value:
Improves forecasting accuracy and helps leadership make informed investment and expansion decisions
# Database Schema Design (Three Related Tables)
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/13e76ea5-03ea-44c8-be22-4594b0faf91a" />

