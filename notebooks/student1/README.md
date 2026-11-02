# Hourly PM2.5 Estimation Across NSW Monitoring Stations

This notebook applies machine learning to estimate hourly PM2.5
concentrations at six NSW monitoring stations: Earlwood, Liverpool,
Newcastle, Richmond, Wollongong, and Wyong.

## Data and evaluation

- Data period: 2016–2025
- Training: 2016–2023
- Validation and model selection: 2024
- Final test: 2025
- Evaluation metrics: MAE, RMSE, and R²

The analysis includes baseline comparisons, regression models,
LightGBM interpretation, PM10 sensitivity analysis, and station-level
evaluation.

## How to run

1. Open the submitted `.ipynb` notebook in Google Colab.
2. Run the dependency-installation cell.
3. Mount Google Drive using the provided cell.
4. Place the 60 input `.xls` files in a folder on your Drive.
5. Update `AIR_QUALITY_DIR` to point to that folder.
6. Run all remaining cells in order.

## Input data

The notebook requires the original NSW air-quality and meteorological
Excel files. These files are not embedded in the notebook.

Expected filenames follow the pattern `Station-Year.xls`,
for example `Earlwood-2016.xls`.

## Scope

This component estimates hourly PM2.5 using historical PM2.5,
current PM10, and meteorological information. It does not perform
multi-step-ahead forecasting or identify wildfire smoke specifically.
