# Air Quality Analysis 

An end-to-end Excel-based air quality analysis workflow applied to a real-world pollution dataset covering 14 Indian cities, executed in Microsoft Excel Online.

---

## Executive Summary

This project documents a complete data analysis pipeline applied to a 10,220-row, 11-column air quality dataset spanning 14 Indian cities over 2022–2023. The raw data was assessed for quality and completeness, enriched with seven engineered features to support time-based and categorical analysis, and explored through PivotTables and PivotCharts to surface city-level, seasonal, and time-based pollution patterns.

Using a workflow built around a consistent three-part procedure — quality assessment via column-by-column audit, feature engineering to unlock deeper analysis, and exploratory analysis via PivotTables and PivotCharts — every column was confirmed to be under 1% missing and retained in full, seven new analytical features were added, and pollution trends were identified across cities, seasons, months, and weekday/weekend splits.

The findings are presented through a single-page professional Excel dashboard, and are ready to support pollution monitoring, seasonal planning, and city-level policy prioritization use cases, once the known limitations (below) are accounted for.

---

## Business Problem

Environmental monitoring data — collected continuously across cities, sensors, and seasons — is only useful if it can be trusted and interpreted at a glance. Left unexamined, air quality data can hide meaningful differences between cities, mask seasonal spikes, and bury the insights that matter inside a spreadsheet of raw pollutant readings.

This project simulates that exact scenario: a real-world air quality dataset assessed for quality, enriched with derived features, and explored using a reproducible Excel workflow so that pollution trends, city rankings, and seasonal patterns can be trusted and communicated through a dashboard, rather than left buried in raw records.

---

## Methodology

The project follows a standard five-stage air quality analysis methodology, with every step governed by one consistent rule: no value is dropped, imputed, or modified without evidence supporting the decision.

**Decision Framework — Retain vs. Flag vs. Engineer**

| Treatment | When Used |
|---|---|
| **Retain as-is** | Value is present, plausible, and requires no correction (applied to all pollutant/weather readings, including extreme highs) |
| **Engineer (derived column)** | A deterministic relationship exists elsewhere in the row (e.g. `Season` derived from `Month Number`) |
| **Flag /document** | A tool limitation prevents a cleaner solution (e.g. Excel Online's slicer and text-box linking constraints) |

**Pipeline stages:**

1. **Data Quality Assessment** — audited all 11 columns for total records, missing values, percentage missing, minimum/maximum values, data type, and unique values, establishing a control baseline of 10,220 records across 14 cities
2. **Feature Engineering** — added seven derived columns (`Year`, `Month Number`, `Month Name`, `Quarter`, `Season`, `AQI Category`, `Weekday/Weekend`) to unlock PivotTable-based time and category breakdowns
3. **Outlier Assessment** — reviewed extreme values across all pollutant and weather columns, confirmed no impossible readings, and retained naturally occurring high-pollution spikes rather than removing them
4. **Exploratory Data Analysis** — built PivotTables and PivotCharts covering city, seasonal, monthly, year-over-year, weekday/weekend, and correlation-based views of the data
5. **Dashboard Design** — consolidated the analysis into a single-page Excel dashboard with KPI cards, bar charts, a column chart, a line chart, and a doughnut chart

Every stage followed the same evidence-first principle: no reading was ever discarded or altered without justification, and every derived feature was built from a deterministic relationship already present in the row.

---

## Skills

- **Excel (Microsoft 365 / Excel Online):** Excel Tables, PivotTables, PivotCharts, Conditional Formatting, Data Validation, Excel Functions
- **Data quality diagnostics:** column-by-column missing-value audit, min/max range checks, data-type verification, outlier investigation
- **Feature engineering:** deterministic derivation of time-based and categorical fields (`Season`, `Quarter`, `AQI Category`, `Weekday/Weekend`) from existing columns
- **Exploratory data analysis:** city, seasonal, monthly, year-over-year, and weekday/weekend comparisons; correlation analysis between AQI, temperature, and humidity
- **Dashboard design:** KPI cards, bar/column/line/doughnut charts, single-page layout design
- **Documentation and auditability:** dataset control totals, transparent treatment of outliers and known tool limitations
- **Tools:** Microsoft Excel Online (Microsoft 365)

---

## Results

| Metric | Result |
|---|---|
| Records analyzed | 10,220 |
| Cities covered | 14 |
| Period covered | 2022–2023 |
| Columns with missing data | All columns, each under 1% missing |
| Values dropped or imputed | 0 (all values retained) |
| Features engineered | 7 (`Year`, `Month Number`, `Month Name`, `Quarter`, `Season`, `AQI Category`, `Weekday/Weekend`) |
| Highest average AQI (city) | Delhi — 247.9 |
| Lowest average AQI (city) | Bengaluru — 68.4 |
| Most common AQI category | "Satisfactory," followed by "Moderate" |
| Highest-AQI season | Winter |
| Highest-AQI month | December |
| Pollutants most correlated with city ranking | PM2.5 and PM10, led by Delhi and Kanpur |
| AQI trend, 2022 → 2023 | Slight increase |
| Weekday vs. weekend AQI | Nearly identical |
| AQI vs. temperature / humidity | Moderate negative correlation with both |

**Findings by analysis stage:**

| Stage | Finding | Basis |
|---|---|---|
| Data Quality Assessment | Dataset assessed as good overall quality | All columns under 1% missing |
| Feature Engineering | 7 new columns added | Derived from `Date` and pollutant/AQI fields |
| Outlier Assessment | No impossible values found | Full review of pollutant and weather ranges |
| EDA — City Comparison | Delhi highest, Bengaluru lowest average AQI | PivotTable by city |
| EDA — Seasonal/Monthly | Winter and December highest average AQI | PivotTable by season and month |
| EDA — Temporal | AQI slightly higher in 2023 than 2022 | Year-over-year PivotTable |
| EDA — Weekday/Weekend | No meaningful difference | Weekday vs. weekend PivotTable |
| EDA — Correlation | Moderate negative correlation with temperature and humidity | Correlation analysis |

---

## Business Recommendations

1. **Prioritize Delhi and Kanpur for pollution-reduction interventions.** These cities consistently led both AQI and PM2.5/PM10 readings. Any city-level abatement budget or policy pilot should weight these two cities first, since they show the largest and most consistent gap versus the rest of the dataset.

2. **Build a seasonal response plan centered on winter, especially December.** Since winter — and December specifically — showed the highest average AQI of any season or month, resource allocation (public advisories, traffic restrictions, monitoring frequency) should scale up ahead of and during this window rather than being applied uniformly year-round.

3. **Treat "Satisfactory" and "Moderate" as the operating baseline, not a target state.** These were the two most common AQI categories across the dataset, meaning typical conditions already sit in the lower-quality half of the AQI scale. Reporting should distinguish "baseline" days from genuinely good-air days rather than treating "Satisfactory" as a success outcome.

4. **Do not rely on weekday/weekend patterns to explain AQI variation.** Since weekday and weekend AQI values were nearly identical, initiatives assuming traffic-driven weekday spikes (e.g. weekend-only restrictions) are unlikely to move the needle; investigation should focus on seasonal and city-level drivers instead.

5. **Use temperature and humidity as leading indicators, not standalone predictors.** The moderate negative correlation between AQI and both weather variables suggests they carry some predictive value for forecasting elevated-AQI days, but the relationship is not strong enough to substitute for direct pollutant monitoring.

6. **Migrate dynamic dashboard elements to desktop Excel or Power BI where possible.** Excel Online's inability to move slicers across worksheets or link text boxes dynamically to cells constrained the dashboard's interactivity. A desktop Excel or Power BI environment would remove this limitation for future iterations.

---

## Repository Contents

- `README.md` — this report
- Raw dataset export, enabling row-by-row verification of the feature engineering and analysis against this documented procedure
- Excel workbook — full dashboard file including raw data, feature-engineered table, PivotTables, PivotCharts, and the final single-page dashboard
- Project report — detailed project report describing the quality assessment, feature engineering, EDA process, and final insights

---

**Author:** Chandrachud Sahi
**Dataset:** Air Quality Data (synthetic, generated with Claude)
**Environment:** Microsoft Excel Online (Microsoft 365)
