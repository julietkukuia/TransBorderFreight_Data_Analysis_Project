# Freight Transportation Analytics Project – Bureau of Transportation Statistics

## Project Overview

This project analyzes freight transportation data from the Bureau of Transportation Statistics (BTS) to uncover inefficiencies, identify emission patterns, and deliver actionable insights to improve logistics, sustainability, and economic performance. The analysis follows the CRISP-DM methodology and combines Python for data processing with Power BI for visualization.

## Business Objectives

The goal is to uncover inefficiencies, trends, and actionable recommendations across transportation systems. The key analytical questions include:

1. Which transportation modes account for the highest freight volume and economic value across months?
2. What is the monthly distribution of freight-related carbon emissions by transportation mode?
3. Which U.S. ports or districts (DEPE) experience the highest freight volumes and costs?
4. Is there a correlation between freight volume (SHIPWT), value (VALUE), and emissions?
5. How does the use of containerisation (CONTCODE) affect freight efficiency and charges?
6. Which commodities (COMMODITY2) and transport modes contribute most to CO2 emissions?
7. How do seasonal patterns affect freight movement efficiency and environmental outcomes?


## CRISP-DM Methodology

### 1. Business Understanding

The BTS seeks to improve transportation efficiency and sustainability. This project supports that by analyzing freight volumes, values, emissions, and container usage across transport modes and seasons.

### 2. Data Understanding

* Data Source: BTS freight datasets (2021–2024), organized by month/year.
* Key Variables: `SHIPWT`, `VALUE`, `EMISSIONS`, `CONTCODE`, `MODE`, `COMMODITY2`, `MONTH`, `YEAR`.

### 3. Data Preparation (Python)

* Merged monthly files across years into one dataset.
* Removed nulls and duplicates.
* Converted data types (e.g., dates, numerical fields).
* Created date dimension for time-based analysis.
* Added computed columns like `Emmisions`, `Freight Charges per Commodity`.

### 4. Modeling

* Applied DAX measures in Power BI for KPIs and metrics:

  * Total Freight Volume
  * Economic Value of Freight
  * New columns relevant for the visualization (`Shipment ID`, `Freight Charges per Commodity`, etc.)
  * Total Emissions
  * Freight Charges per Commodity
  * Containerization Efficiency
* Time-based modeling using DimDate for trends.

### 5. Evaluation

Power BI dashboards were created to visualize:

* Freight volume and value by mode.
* Monthly emissions trends.
* Correlation between volume, value, and emissions.
* Impact of container usage on efficiency.
* Top commodities contributing to emissions.

### 6. Deployment

Final deliverables include:

* Power BI report (interactive dashboards)
* README
* Python scripts (data prep and EDA)
* Presentation file (business questions, methods, insights)

## Tools Used

| Tool     | Purpose                                   |
| -------- | ----------------------------------------- |
| Python   | Data merging, cleaning, and preprocessing |
| Pandas   | Data transformation                       |
| Power BI | Dashboard development                     |
| DAX      | Custom measures and KPI modeling          |
| GitHub   | Version control and documentation         |

## Key Accomplishments

* Delivered a comprehensive dashboard with actionable insights across transport modes.
* Modeled and visualized CO2 emissions patterns by commodity and season.
* Identified inefficiencies and high-cost patterns across shipment types.
* Integrated date modeling and created dynamic KPIs in Power BI.

## Project Structure

```
├── /data
│   └── Merged & cleaned freight data files (Python)
├── /scripts
│   └── data_prep_and_eda.ipynb
├── /powerbi
│   └── BTS_Freight_Insights.pbix
├── /presentation
│   └── Final_Insights_Presentation.pptx
├── README.md


> Analyst: Juliet Fafali Kukuia
> Team: getINNOtized Data Analytics  
> Client: BTS – U.S. Department of Transportation
