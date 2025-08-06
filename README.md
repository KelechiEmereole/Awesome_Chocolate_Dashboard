# Empowering Sales Decisions at Awesome Chocolate: A Power BI Dashboard Project

## Dashboard Snapshots

Here’s a preview of the Power BI dashboard used in this project:

![Dashboard](https://github.com/KelechiEmereole/Awesome_Chocolate_Dashboard/blob/main/Awesome%20dashboard%20screenshot.PNG?raw=true)


## Table of Contents
1. [Introduction](#introduction)
   
2. [Project Aim](#project-aim)

3. [Project Description](#project-description)

4. [Data Acquisition and Preparation](#data-Acquisition-and-preparation)

5. [Data Cleaning and Transformation](#data-cleaning-and-transformation)

6. [Data Analysis and Visualization](#data-analysis-and-visualization)

7. [Insights and Interpretation](#insights-and-interpretation)

8. [Recommendations](#recommendations)

9. [Skills Demonstrated](skills-demonstrated)

## Introduction

In today's fast-paced consumer market, data-driven decision-making is essential for companies aiming to stay competitive. This project focuses on Awesome Chocolate, a premium chocolate manufacturer looking to uncover key business insights using data analytics.

The goal is to provide stakeholders with an interactive and insightful Sales Performance Dashboard that offers a comprehensive view of sales operations — from revenue generation to individual salesperson performance, product categories, and shipment trends.

By visualizing this data through an intuitive Power BI dashboard, the project demonstrates how modern business intelligence tools can empower organizations to make informed, strategic decisions that drive growth and efficiency.

## Project Aim

The primary aim of this project is to design an interactive and visually engaging Power BI dashboard for Awesome Chocolate that:

* Tracks and analyzes overall sales performance.

* Evaluates the contribution and effectiveness of each salesperson.

* Monitors performance across different product categories and individual products.

* Examines the efficiency and volume of shipment deliveries.

* Supports data-driven decision-making by presenting key performance metrics in a digestible and actionable format.

This dashboard is intended to help stakeholders gain quick insights into sales trends, identify growth opportunities, and optimize operations for improved profitability.

## Data Acquisition and Preparation

The dataset used for this dashboard was provided in an Excel format and contains sales-related information for Awesome Chocolate. It captures transaction-level data, enabling a granular 

view of sales operations across products, personnel, and geographies.

Key Columns in the Dataset:
Sales Person – Name of the individual responsible for the sale.

Geography – Country where the sale occurred (e.g., USA, UK, New Zealand).

Product – Specific chocolate product sold (e.g., Raspberry Choco, 85% Dark Bars).

Date – The date the transaction occurred.

Sales – Total revenue generated from the transaction (in USD).

Boxes – Number of chocolate boxes sold in the transaction.

## Data Cleaning and Transformation

To ensure accuracy and consistency, the dataset underwent the following transformations:

Removed missing or irrelevant entries (e.g., null shipment dates).

Standardized date formats and linked with a calendar table for time intelligence calculations.

Calculated key metrics such as:

      * Total Boxes, Sales, Costs, Profit, and Shipments for both latest and previous months.

      *  Month-over-Month (MoM) Change % for all key KPIs.

      * Profit %, Targets, and Indicators to track performance against goals.
      
Dynamic Measure Selection:

A disconnected table called Measure Selector was created using the following DAX formula:
       Measure Selector = {
    ("Sales", NAMEOF('Measure'[Total Sales]), 0),
    ("Boxes", NAMEOF('Measure'[Total Boxes]), 1),
    ("Cost", NAMEOF('Measure'[Total Cost]), 2),("Shipment", NAMEOF('Measure'[Total shipment]), 3),
    ("Proft", NAMEOF('Measure'[Total Proft]), 4)}
    
This provides flexibility for stakeholders to view the metric that matters most to them — all within the same visual.

## Data Analysis and Visualization

Once the dataset was cleaned and transformed, interactive and insightful visualizations were built in Power BI to uncover key business trends and support data-driven decision-making. The key components include:

### 1. Interactive Dashboard
A visually engaging dashboard was developed to allow users to explore sales performance across multiple dimensions in real time.

### 2. Dynamic KPI Cards

Key performance indicators—Total Sales, Total Boxes, Total Cost, Total Shipment, and Total Profit—were displayed using dynamic cards. A Measure Selector was implemented to let users switch seamlessly between different KPIs.

### 3. Time Series Visualization

Line charts were used to show monthly trends, helping reveal patterns and seasonality in sales and box distributions over time.

### 4. Bar Charts

A bar chart was created to display shipment breakdown by number of boxes shipped, providing a clear view of shipping volume trends and fulfillment activity.

### 5. Profit Gauge

A gauge chart clearly shows the total profit achieved, helping users instantly assess profitability status.

### 6. Filters and Slicers

Slicers were added to allow flexible filtering across:

  * Product Category

  * Geography Cities

  * Selected KPI (via Measure Selector)

### 7. Bookmarks for Table Views

Bookmarks were set up to toggle between two key tables:

   * Salesperson Performance

   * Product Performance
   * 
This feature enables focused views for stakeholders interested in specific contributors.

## Insights and Interpretation

The dashboard provided a clear overview of Awesome Chocolate's sales performance, product profitability, and operational efficiency across time, product categories, and geography. Below 

are key insights extracted from the data analysis:

### Overall Performance

Total Sales: $34M

Total Boxes Sold: 2M

Total Shipments: 6K

Total Cost: $13.5M

Total Profit: $20.5M

The company is maintaining a healthy profit margin with approximately 60.3% profit target achieved.

### Monthly Performance Trends

Highest Sales Month: December with $2.9M in sales and the second to highest shipment count of 529.

Highest Shipment Month: January with 592

Consistent Performance: Most months showed steady sales between $2.3M–$2.9M, with strong profitability.

Profit Margins: Averaging between 1.3M – 1.8M monthly, showing healthy cost management.

### Product Category Performance

Bars led in both sales and profit:

Sales: $17.1M | Profit: $10.4M

Followed by Bites: $10.1M in sales and $6.2M profit.

The "Other" category also contributed $6.8M in sales and $3.9M in profit.

### Geographic Insights

Each geography contributed evenly with slight variation:

Top Performing Regions:

New Zealand: $5.9M sales | $3.6M profit

Australia & Canada: $5.7M sales each, with over $3.6M and $3.4M in profit respectively

Most Profitable: Australia at $3.6M in profit with slightly lower cost base.

### Best-Performing Products

Peanut Butter Cubes:

Sales: $2.03M | Profit: $1.77M | Profit Margin: 87.1%

99% Dark & Pure:

Sales: $1.98M | Profit: $1.46M | Margin: 74%

Manuka Honey Choco:

Sales: $1.84M | Profit: $1.45M | Margin: 78.9%

These products significantly outperform the target margin, indicating strong customer preference and effective pricing.

### Underperforming Products

Drinking Cocoa:

Sales: $1.42M | Profit: $379.1K | Margin: 26.7%

50% Dark Bites:

Sales: $1.33M | Profit: $363.1K | Margin: 27.2%

Baker’s Choco Chips:

Sales: $1.47M | Profit: $225.3K | Margin: 17.4%

These may need cost restructuring, repositioning, or marketing support.

### Salesperson Performance

Top Performers:

Kelci Walkden: $1.52M sales | $998.3K profit | Margin: 65.1%

Rafaelita Blaksland: $1.5M sales | $958.8K profit | Margin: 63.8%

Husein Augar: $1.47M sales | $926.9K profit | Margin: 62.9%

Bottom Performers:

Ches Bonnell: Lowest profit margin at 53.6%

Andria Kimpton and Madelene Upcott also underperformed on profit targets.


## Recommendations

* Double Down on High Performers : Leverage the strengths of top salespersons like Kelci Walkden and focus on high-profit products such as Peanut Butter Cubes to drive further growth.

* Support Low-Performing Regions : Investigate reasons behind lower performance in regions like the UK and consider targeted promotions or operational improvements.

* Improve Shipment Efficiency : Months like February had the lowest shipment volume — assess logistics or seasonal trends to ensure consistent delivery.

* Use the KPI Selector for Targeted Monitoring : Encourage team leads to utilize the Measure Selector to track metrics that matter most — like Sales, Boxes, Cost, and Profit — ensuring focus and accountability.

* Optimize Product Portfolio : Reevaluate low-performing products such as Drinking Cocoa. Consider marketing support, pricing strategies, or even phasing out underperformers.

* Utilize Bookmarks for Dynamic Presentations : Your Salesperson and Product bookmarks can enhance storytelling in reviews. Use them to spotlight team performance or product trends.

## Skills Demonstrated

* Power BI (DAX, Power Query, Bookmarks)

* Data Modeling & Relationship Design

* KPI and Measure Creation

* Dynamic Interactivity (via slicers, bookmarks)

* Business Insight Generation

* Dashboard Documentation & Presentation

<br/><br/>

**Thank you for taking the time to read this report!**

**Please reach out for any updates.**

### Author
[Kelechi Emereole](https://github.com/KelechiEmereole)

### Author
[Kelechi Emereole](https://github.com/KelechiEmereole)
