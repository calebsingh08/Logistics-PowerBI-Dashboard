# Logistics & Shipment Performance Dashboard

## Project Overview

This project is an interactive Power BI dashboard designed to analyze logistics and shipment performance using a simulated shipment dataset.


## The dashboard focuses on:
- Shipment tracking KPIs
- Revenue analysis
- Delayed shipment monitoring
- Carrier performance
- Regional operational insights
- Interactive reporting using slicers and report tooltips
- Power BI Service deployment
- Gateway and refresh configuration concepts
- Business Problem


## Logistics organizations require centralized reporting to monitor:
- Shipment volumes
- Delayed deliveries
- Revenue generation
- Carrier efficiency
- Regional shipment performance

This dashboard provides an executive-level overview to support operational decision-making and shipment analysis.

## Dataset Source

The dataset used for this project was sourced from Kaggle and further modified for analytical and reporting purposes.


## Randomized and varied values were additionally introduced to:
- simulate realistic logistics scenarios
- improve KPI diversity
- support interactive reporting and visualization analysis


## Dataset preparation included:
- data cleaning
- formatting
- KPI-based measure creation
- reporting optimization for Power BI dashboards

## Dataset Information

A logistics shipment dataset sourced from Kaggle was used and further modified to simulate realistic shipment operations and reporting scenarios.


## Dataset Includes:
- Shipment IDs
- Regions
- Carriers
- Revenue
- Shipping Cost
- Delivery Status
- Delay Indicators
- Customer Ratings
- Distance Covered
- Product Categories
- Shipment Modes
- Shipment Dates

## Randomized values were intentionally generated to:
- create realistic business scenarios
- support KPI analysis
- improve dashboard storytelling
- simulate operational shipment trends

## Data Preparation
### Tables Used
- Main Dataset
- fact_shipments

Contains shipment transaction-level data.

- Date Table
- Dim_Date

Created for future scalability and time-based reporting purposes and includes
- Date
- Month
- Quarter
- Year
- Measures Table


A dedicated Measures table was created following Power BI best practices to centralize all DAX measures and KPIs for:

- cleaner model organization
- better maintainability
- improved readability


### Measures Moved Into Measures Table
- Total Revenue
- Total Shipments
- Total Shipping Cost
- Delayed Shipments
- On Time Delivery %

### DAX Measures Used
- Total Revenue
- Total Revenue = SUM(fact_shipments[Revenue]) which calculates total shipment revenue.
- Total Shipments = COUNT(fact_shipments[order_id]) which calculates total shipment count.
- Delayed Shipments = CALCULATE(COUNT(fact_shipments[order_id]),fact_shipments[is_delayed] = "yes") which counts delayed shipments.
- On time delivery % =
- DIVIDE(CALCULATE(COUNT(fact_shipments[order_id]),fact_shipments[is_delayed] = "no"),COUNT(fact_shipments[order_id])) which calculates percentage of on-time deliveries.
- Total Shipping Cost = SUM(fact_shipments[shipping_cost]) which calculates total shipping expenses.

## DAX Concepts Demonstrated

### This project demonstrates usage of:
- CALCULATE()
- SUM()
- COUNT()
- DIVIDE()
- Filter Context
- KPI Calculations
- Dashboard Features
- KPI Cards

## Executive KPIs displayed:
- Total Shipments
- Shipping Cost
- Delayed Shipments
- Customer Ratings
- On-Time Delivery %
- Total Revenue
- Interactive Slicers

## Slicers added for:
- Region
- Carrier
- Product Category

Allows dynamic dashboard filtering.

## Visualizations Used
- Revenue by Region - Bar chart analyzing regional revenue contribution.
- On-Time vs Delayed Performance - Donut chart comparing shipment delivery performance.
- Total Shipments by Carrier - Bar chart evaluating shipment distribution across carriers.
- Performance by Region & Carrier - Matrix table displaying:

a) Revenue
b) Shipment Count
c) On-Time Delivery %
d) Delayed Shipments
e) Report Tooltip Implementation

## A custom tooltip page was created:
Tooltip - Region

## Tooltip Includes:
- Revenue KPI
- Delayed Shipment KPI
- Customer Rating KPI
- Top 5 carriers by revenue

The tooltip dynamically changes based on the selected region.

## Purpose of tooltip implementation:
- reduce dashboard clutter
- improve user experience
- provide contextual insights on hover
- enhance dashboard interactivity

## Power BI Service Deployment

### The dashboard was published to Power BI Service for:

- cloud accessibility
- report sharing
- refresh configuration
- gateway integration
- Gateway & Refresh Concepts

### An On-Premises Data Gateway was configured to explore:

- local file connectivity
- scheduled refresh setup
- semantic model refresh concepts

### Concepts explored:

- semantic models
- gateway connections
- refresh scheduling
- Power BI Service integration

## Potential future improvements:

- Incremental Refresh
- Row Level Security (RLS)
- Drillthrough Pages
- Bookmark Navigation
- SQL Integration
- DirectQuery
- Enterprise Semantic Models
- Mobile Layout Optimization

### Author
Caleb Singh
