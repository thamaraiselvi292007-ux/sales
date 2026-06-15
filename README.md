# sales
## Overview
sales_dashboard is a Power BI project designed to analyze sales and revenue data using interactive dashboards and visualizations.

## Features
- Total Sales KPI
- Total Revenue KPI
- Revenue Trend Analysis
- Product Performance Analysis
- Revenue Distribution by Category
- Interactive Filters and Slicers

## Dataset Files
### Customers.csv
Contains customer information:
- CustomerID
- CustomerName
- City

### Products.csv
Contains product information:
- ProductID
- ProductName
- Category
- Price

### Sales.csv
Contains sales transaction details:
- SaleID
- CustomerID
- ProductID
- Quantity
- Date

## Data Model
Relationships used:
- Customers[CustomerID] → Sales[CustomerID]
- Products[ProductID] → Sales[ProductID]

## Revenue Calculation
```DAX
Revenue = Sales[Quantity] * RELATED(Products[Price])
