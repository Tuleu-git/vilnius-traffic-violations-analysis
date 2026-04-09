# Analysis of Parking and Traffic Violations in Vilnius (2018–2025)

## Project Overview
This research project analyzes urban mobility and traffic violation patterns in **Vilnius, Lithuania**, using official administrative open data. By processing over **675,000 records**, the study employs a combination of **Python** and **SQL** to test five core hypotheses regarding the timing, location, and characteristics of traffic offenses.

The analysis provides evidence-based insights into traffic management, highlighting peak violation periods and high-density geographic clusters to support urban planning and enforcement strategies.

## Key Hypotheses & Findings
* **Weekday vs. Weekend:** Confirmed that traffic violations occur **significantly less frequently on weekends** than on weekdays (Mean: 154.4 vs. 320.3).
* **Vehicle Type:** Non-electric vehicles account for **96.3% of all violations**. While the count is significantly higher, this also reflects the broader vehicle population in Vilnius.
* **City Center Concentration:** Proved that the majority of violations (**53%**) occur within a **2 km radius of the city center** (Cathedral Square).
* **Temporal Peaks:** Identified **lunchtime (12:00–14:00)** as a high-pressure period, with violation rates 124% higher than expected under a uniform distribution.
* **Seasonal Trends:** Found **no consistent seasonal pattern**; violation levels fluctuate year-to-year rather than exhibiting a clear "summer peak".

## Data Source & Attribution
* **Dataset:** [Parkavimo ir kelių eismo taisyklių pažeidimai Vilniaus mieste](https://data.gov.lt/datasets/3874/).
* **Publisher:** Valstybės duomenų agentūra (State Data Agency).
* **Provider:** Vilniaus miesto savivaldybės administracija (Vilnius City Municipality).
* **License:** [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
* **Note:** This analysis is an independent adaptation of the original data and is not endorsed by the licensor.

## Technologies Used
* **Languages:** Python, SQL (MySQL, SQLite, DuckDB).
* **Data Processing:** Pandas, NumPy.
* **Statistical Analysis:** SciPy (Permutation tests, Mann-Whitney U, Chi-Square, Bootstrap CIs).
* **Geospatial Visualization:** Folium (Heatmaps), GeoPandas, Shapely.
* **Visualization:** Matplotlib, Seaborn (APA 7th edition styling).

## Project Workflow
1. **Data Cleaning:** Handled missing values, standardized timestamps, and removed invalid future-dated records.
2. **Feature Engineering:** Generated indicators for weekends, Lithuanian public holidays, and "City Center" proximity.
3. **Exploratory Data Analysis (EDA):** Performed spatial clustering and temporal aggregation using both Python and SQL for methodological cross-check.
4. **Hypothesis Testing:** Evaluated research questions using non-parametric statistical methods to ensure robustness against non-normal data distributions.

## Installation & Requirements
To replicate this analysis, install the following dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy duckdb folium geopandas shapely mysql-connector-python holidays
```

## Limitations
* **Enforcement Bias:** The data reflects *recorded* violations, which may be influenced by changes in police patrol intensity or reporting policies rather than driving behavior alone.
* **Data Completeness:** Some records lacked geographic coordinates (approx. 20% of the raw dataset), requiring cleaning for spatial analysis.
* **Population Context:** Vehicle type findings reflect raw counts; a more precise analysis would require per-capita vehicle registration data for Vilnius.

***

**Author:** Ablaikhan Tuleu
