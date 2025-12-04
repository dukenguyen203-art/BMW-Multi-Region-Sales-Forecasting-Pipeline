# BMW-Multi-Region-Sales-Forecasting-Pipeline
*Time-Series Forecasting - Prophet - Python*
## Overview
This project builds an end-to-end forecasting pipeline to analyze and predict annual BMW sales across global regions and vehicle models. It replicates a real-world analytics workflow, from raw data to backtesting to forward-looking insights, using Python, Prophet, and multi-panel visualisations.
The goal of this project is to genereate liable 5-year forecasts for BMW vehicle sales while evaluating model performance across 66 independent Model x Region time series.

The workflow includes:
- Exploratory Data Analysis (EDA)
- Time-series aggregation (Model × Region × Year)
- Backtesting using an 80/20 temporal split
- Forecast evaluation (MAE, RMSE, MAPE)
- Full-history retraining and forecasting
- Visualisation using a shared-axis forecast matrix
- Executive insights + data-driven recommendations

This project demonstrates both technical execution and business-oriented analytical reasoning.

## Dataset Summary
This project uses a curated dataset of **BMW Worldwide Sales Records (2010–2024)**, covering major global regions and key vehicle attributes. 
- [BMW Worldwide Sales Records (2010–2024)](https://www.kaggle.com/datasets/ahmadrazakashif/bmw-worldwide-sales-records-20102024)

Key fields
- Model – BMW vehicle line (e.g., 3 Series, X5)
- Year – 2010–2024
- Region – Asia, Europe, North America, South America, Middle East, Africa
- Engine_Size_L, Fuel_Type, Transmission, Mileage_KM
- Price_USD – Vehicle price
- Sales_Volume – Units sold (target for forecasting)

The dataset enables analysis of long-term market trends, regional demand differences, and forecasting of future BMW sales.

## Project Workflow
1. Data Loading & EDA
  - Load raw BMW dataset
  - Generate a reusable EDA summary
  - Validate data consistency and export cleaned fact table (Parquet)
2. Time-Series Preparation & Backtesting
  - Aggregate Model × Region × Year sales
  - Apply 80/20 time-based train/test split
  - Fit Prophet on each segment
  - Evaluate MAE, RMSE, and MAPE
  - Visualize segment-level accuracy using a MAPE heatmap
3. Full-History Forecasting
  - Retrain Prophet using the full dataset
  - Produce 5-year forecasts for all segments
  - Build a shared-axis, multi-panel forecast matrix
  - Color forecasts by accuracy confidence (MAPE categories)
4. Insights & Recommendations
  - Highlight strong vs. volatile forecasting regions
  - Identify segments suitable for precise planning
  - Recommend scenario modeling and advanced hybrid methods for unstable markets

## Key Visuals
**Model Performance (MAPE Heatmap)**
<img width="754" height="584" alt="image" src="https://github.com/user-attachments/assets/21455488-0f29-40c7-b21b-795b9dd5abb4" />

**Forecast Matrix (Actual vs Predicted)**
<img width="2384" height="3295" alt="image" src="https://github.com/user-attachments/assets/460ccc41-30aa-4281-b0d9-977a2f8ea614" />

## Insights and Recommendations
- Most segments achive a strong forecasting performance (median MAPE ~ 15%).
- High-confidence regions/models can support stable production and sales planning.
- Volatile segments (e.g., X5/X6 in Asia/Europe) require scenario-based forecasts.
- Incorporateing external driveers (economic indicators, fuel prices) can strengthen accuracy.
- High-volume segments require closer monitoring due to higher business impact.

## Tech Stack
- Python: pandas, numpy, Prophet, seaborn, matplotlib
- Modeling: Time-series forecasting per Model × Region segment
- Evaluation: MAE, RMSE, MAPE with sorted accuracy heatmaps
- Reporting: Multi-panel forecast grids
- Output: Cleaned parquet files for integration with Power BI

## Forecasting Pipeline
Access and download the detailed pipeline
- [BMW Multi-Region Sales Forecasting Pipeline]()

## Conclusion 
This project delivers a complete forecasting workflow that processes raw BMW sales data, evaluates Prophet across 66 Model × Region segments, and produces 5-year forecasts supported by structured visualisations and actionable insights. The model performs well in most segments, provides reliable forward-looking guidance, and highlights areas of high uncertainty. The final system forms a strong foundation for scalable forecasting, with clear pathways for enhancement using external drivers or hybrid ML methods.

## Author
Duke Nguyen
* Github: [@dukenguyen203-art](https://github.com/dukenguyen203-art)
* LinkedIn: [Duke Nguyen](https://www.linkedin.com/in/duke-n-nguyen/)

