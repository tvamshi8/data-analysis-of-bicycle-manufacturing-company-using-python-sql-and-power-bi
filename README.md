# Data Analysis of Bicycle Manufacturing Company Using Python, SQL and Power BI
 
## Overview

This project provides a comprehensive Production and Inventory Analysis of the Microsoft AdventureWorks Database. Adventure Works is a fictional bicycle manufacturing company, and this database contains standard transactions data from an Enterprise Resource Planning (ERP) System. It includes data from various company scenarios: Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Administration.

This analysis specifically focuses on the Manufacturing and Inventory segments of the data. Microsoft Power BI has been utilized to create an interactive dashboard, pulling data directly from SQL Server to provide actionable business insights.

## Data Source

[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Data Model

Defining an effective data structure in a dashboard is critical. This project incorporates a star schema model to ensure efficient design and faster data refresh rates. The image below illustrates the tables used in the process:

<img width="1024" alt="DataModel" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/DataModel.png">

### Tables used in the model:

- Production Location - Contains production assembly data, i.e. parts used to manufacture each product are defined here with an assembly location category.
- Production Product - Data related to products, including physical details and pricing.
- Production ProductCategory - Products and their defined categories.
- Production ProductSubcategory - Products and their specific subcategories.
- Production ProductInventory - Inventory data for the produced products.
- Production ScrapReason - Waste data related to manufacturing processes.
- Production WorkOrder - Production transactions and related operational data.
- Production WorkOrderRouting - Production work order scheduling details.
- Sales SalesOrderDetail - Transactional sales data for performance comparison.

## Built With

- [Python](https://www.python.org/)
- [Power BI](https://powerbi.microsoft.com/en-us/)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

## Analysis

### Main Page

This dashboard analyzes manufacturing and inventory operations through an app-like navigational interface. The main page serves as a hub leading to two primary areas: Production Overview and Inventory Overview. Each section breaks down specific details and KPIs on subsequent pages.

<img width="1024" alt="Main Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Main%20Page.png">

### Production Overview

<img width="1024" alt="Production Overview Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20Page.png">

The dashboard is structured according to fiscal year terms. A custom date table was created using DAX to automatically generate fiscal year segregations, assuming the fiscal year starts on October 1st and ends on September 30th.

This page provides a high-level manufacturing overview. Custom measures were created in Power BI to track specific KPIs. All charts and KPIs are described below:

<img width="1024" alt="Production Overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20KPI.png">

### Charts on the page

* Cumulative Multiline chart: Showing production totals helps compare fiscal year production trends and assists in identifying manufacturing bottlenecks.

<img width="1024" alt="Cumulative Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Cumulative_Monthly_totals_by_fiscal_year.jpg">

* Donut Chart: Displays actual cost distribution across different parts of the assembly line. This helps determine which components drive costs and where improvements are needed to reduce production expenses.

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Actual%20Cost%20of%20production%20by%20Assembly%20location.jpg">

* Waste cost by year line chart: A visualization showing the financial impact of discarded products and the overall trend in manufacturing waste.

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste%20cost%20by%20the%20Year.jpg">

### Category Analysis

The Product Category Page allows for a more granular analysis to identify specific issues within the manufacturing system. This section consists of four charts providing in-depth analysis of production components.

<img width="1024" alt="Production Category Analysis" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Category%20Analysis.png">

**Pareto Charts**

The Pareto charts represent frequency and cost, with the most significant categories arranged from left to right. An overlapping line shows the cumulative percentage contribution. This project utilizes two Pareto charts: one for manufacturing components and another for finished bike products.

<img width="1024" alt="Pareto Charts" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Pareto_Charts.jpg">

**Waste Cost - Product Matrix Visual**

This matrix identifies exactly where waste is impacting the company's finances. It categorizes waste by reason and product type (Bikes vs. Components). Conditional formatting highlights the most significant cost drivers.

<img width="1024" alt="Waste Cost" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste_Cost_Matrix.jpg">

**Bar chart**

A visualization showing the volume of product categories produced on time.

<img width="1024" alt="Bar chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/On_time_production_by_category.jpg">

### Inventory Overview

The Inventory Overview analyzes stock levels and value. This analysis assumes a centralized distribution location to evaluate inventory health.

<img width="1024" alt="Inventory data overview" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20data%20overview.png">

**KPIs**

<img width="1024" alt="Inventory data overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20Overview%20KPI.png">

**Area Charts**

These charts display inventory quantity and value by assembly location. They help determine which manufacturing segments hold the most capital. A toggle button allows users to switch between quantity and value views.

**Inventory Turnover Multiline chart**

Comparing inventory turnover across fiscal years reveals trends in inventory utilization, aiding in the optimization of the production process.

<img width="1024" alt="Inventory Turnover Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory_tunrover_chart.jpg">

## Maintainer

**Vamshi Tummala**
Business Analyst

Vamshi is a Business Analyst with experience in transforming operational data and business requirements into reporting solutions and measurable outcomes. With a strong background in SQL, Power BI, and Python, he focuses on strengthening KPI visibility and supporting data-driven planning decisions. He is currently pursuing a Master's degree in Data Science to further specialize in analytics-driven problem solving.

- Email: tummalavamshi266@gmail.com
- LinkedIn: https://www.linkedin.com/in/vamshi-tummala-995948vt/