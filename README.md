<div align="center">

## Air Quality Analysis 

</div>

This project analyzes air quality data collected from 14 Indian cities during 2022–2023. The goal was to assess
the dataset's quality, engineer features that make deeper analysis possible, explore pollution trends across
cities, seasons, and time, identify the most and least polluted cities, and present the findings through a
professional Excel dashboard.

<div align="center">

## Objectives

</div>

Assess the quality and completeness of the dataset.

Engineer features that simplify time-based and categorical analysis.

Explore pollution trends across cities, seasons, and time.

Identify the most and least polluted cities.

Build a professional dashboard for communicating insights.

<div align="center">

## Dataset

</div>

Records: 10,220

Cities: 14

Period: 2022–2023

Variables: Date, City, AQI, PM2.5, PM10, NO2, SO2, CO, O3, Temperature, Humidity

<div align="center">

## Data Quality Assessment

</div>

Every column was checked for total records, missing values, percentage missing, minimum and maximum
values, data type, and unique values. Missing values across every column were under 1%, so the dataset was
assessed as good overall quality and every value was retained rather than dropped or imputed.

<div align="center">

## Feature Engineering

</div>

Seven columns were added to support deeper analysis: Year, Month Number, Month Name, Quarter, Season,
AQI Category, and Weekday/Weekend. These features simplified PivotTable analysis and enabled seasonal,
monthly, and categorical breakdowns that the raw dataset could not support on its own.

<div align="center">

## Outlier Assessment

</div>

Extreme values were reviewed across all pollutant and weather columns. No impossible values were found.
Since air pollution can naturally produce extreme spikes, the observed high values were retained rather than
removed.

<div align="center">

## Exploratory Data Analysis

</div>

EDA was performed using PivotTables and PivotCharts, covering:

Average AQI by city

AQI category distribution

Average AQI by season and by month

Average PM2.5 and PM10 by city

Year-over-year AQI comparison

Weekday vs weekend AQI comparison

Correlation between AQI, temperature, and humidity

<div align="center">

## Dashboard

</div>

A single-page dashboard was built in Microsoft Excel Online, featuring KPI cards (average AQI, average
PM2.5, average PM10, total records), horizontal bar charts, a column chart, a line chart, and a doughnut chart.

<div align="center">

## Key Findings

</div>

Delhi recorded the highest average AQI (247.9); Bengaluru recorded the lowest (68.4).

"Satisfactory" was the most common AQI category, followed by "Moderate."

Winter had the highest average AQI of any season; December had the highest average AQI of any month.

PM2.5 and PM10 followed similar city-wise patterns, led by Delhi and Kanpur.

AQI increased slightly in 2023 compared to 2022.

Weekday and weekend AQI values were nearly identical.

AQI showed a moderate negative correlation with both temperature and humidity.

<div align="center">

## Tools Used

</div>

Microsoft Excel Online (Microsoft 365), Excel Tables, PivotTables, PivotCharts, Conditional Formatting, Excel
Functions, Data Validation, Feature Engineering.

<div align="center">

## Skills Demonstrated

</div>

Data Cleaning, Data Quality Assessment, Exploratory Data Analysis, Feature Engineering, Dashboard Design,
Data Visualization, Business Insight Generation, Documentation, Problem Solving.

<div align="center">

## Challenges Faced

</div>

Learning Excel dashboard creation from scratch, designing a clean layout, choosing appropriate chart types for
each question, organizing multiple worksheets for documentation and analysis, and working around Excel
Online's limitations — it does not support moving slicers across worksheets or linking text boxes dynamically
to cells.

<div align="center">

## Conclusion

</div>

This project demonstrates an end-to-end Excel data analysis workflow — from raw data assessment to
dashboard delivery. It highlights the ability to assess data quality, engineer useful features, perform
exploratory analysis, derive actionable insights, and communicate results effectively through visualization.

<div align="center">

## Contact

</div>

Chandrachud Sahi

[your-email@example.com](mailto:your-email@example.com) — replace with the same mailto link used on your other project READMEs.
