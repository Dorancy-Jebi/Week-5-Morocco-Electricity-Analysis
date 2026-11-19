# Week 5 - Data Analytics Track Submission
## Morocco Electricity Consumption Analysis (Tasks 1-6)

This folder contains the complete Data Analytics Track submission for the Week 5 assignment. It includes an executed, reproducible Jupyter Notebook; the supplied source files; a prepared dataset with requested time features; static and interactive visualizations; a PDF analytical report; and supporting documentation.

## Submission contents

```text
Week5_Data_Analytics_Submission/
├── README.md
├── Data_Quality_and_Methodology.md
├── Business_Insights_and_Recommendations.md
├── requirements.txt
├── analysis_summary.json
├── data/
│   ├── powerconsumption.csv
│   ├── powerconsumption_datadictionary.csv
│   └── powerconsumption_cleaned.csv
├── notebooks/
│   └── Morocco_Electricity_Consumption_Analysis.ipynb
├── reports/
│   └── Morocco_Electricity_Consumption_Analytical_Report.pdf
└── visualizations/
    ├── PNG static charts
    └── standalone Plotly HTML charts
```

## Reproduce the analysis

1. Install Python 3.10 or later.
2. From this folder, create and activate a virtual environment if desired.
3. Install the dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Start Jupyter Notebook or JupyterLab from this folder:

   ```bash
   jupyter lab
   ```

5. Open `notebooks/Morocco_Electricity_Consumption_Analysis.ipynb` and use **Run All**. The notebook discovers the `data/` and `visualizations/` folders relative to the project. It writes the prepared CSV and regenerates its charts.

The notebook has saved outputs from the analysis run so the results can be reviewed without rerunning first. Standalone Plotly charts in `visualizations/` can be opened directly in a browser; they are self-contained and do not require internet access.

## Analysis scope

The notebook completes Tasks 1-6: inspect the dataset and dictionary; validate data quality and 10-minute cadence; prepare a parsed timestamp and Year, Month, MonthName, Day, Hour, DayOfWeek and Date columns; summarize and compare the three zones over daily, weekly, monthly, hourly and weekday periods; analyze temperature, humidity and wind-speed associations; create Matplotlib, Seaborn and Plotly visuals; and present evidence-based findings and recommendations.

## Measurement and interpretation notes

- The extract contains 52,416 observations from 2017-01-01 00:00 through 2017-12-30 23:50. It does not include 2017-12-31.
- No rows were removed and no values were imputed. The cleaned/prepared file contains the original fields plus parsed timestamps and derived time columns.
- The source data dictionary labels the zone fields in kWh, but it does not establish whether one 10-minute reading represents interval energy, average power, or another reporting convention. The analysis therefore reports mean recorded values and does not sum readings into energy totals.
- `GeneralDiffuseFlows` and `DiffuseFlows` are described as atmospheric emissions-gas diffusion measures, but their physical interpretation and units require confirmation. Relationships with these two fields are not interpreted in this submission.
- Correlations are descriptive associations, not causal effects. The dataset covers one year, so it cannot establish stable long-term or year-over-year seasonality.

## Main headline results

- Mean recorded values rank Zone 1 highest (32,344.97), Zone 2 next (21,042.51), and Zone 3 lowest (17,835.41).
- Mean hourly values peak at 20:00 across all zones.
- Zone 1 and Zone 2 reach their highest monthly mean in August; Zone 3 reaches its highest monthly mean in July.
- At the 10-minute observation level, temperature has a moderate positive Spearman association with all zones; humidity has a negative association; wind-speed associations are weakly positive.
- Statistical IQR flags are retained rather than deleted; Zone 3's high flags cluster in July-August evenings and warrant contextual review.

The full limitations, calculations, and recommendations are in the analytical report and the companion Markdown documentation.
