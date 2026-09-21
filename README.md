# India Road Safety Resource Allocation Analysis

## Business Problem
Should traffic enforcement concentrate on rush-hour congestion — or on festival 
days, when celebrations, alcohol consumption, and off-schedule travel spike? 
Without objective data, police and municipal governments risk spreading resources 
too broadly instead of targeting where accidents actually cluster.

## Dataset
20,000 vehicle crash records from 2022–2025 across 8 major Indian cities, 
covering injury level, cause, weather condition, road type, and time period 
for each event.

## Notebook
- `1_EDA_road_accidents.ipynb` — data cleaning, exploratory dashboard analysis
- `2_Reegression_road_accidents.ipynb` — hypothesis testing, and three regression models (Logistic, Multiple Linear, Poisson).

## Methodology
1. Built a Power BI dashboard to explore accident patterns by time, cause, weather, 
   and city before formal testing
2. Tested two hypotheses using T-tests:
   - **Peak hours** (7–10 AM, 5–8 PM) vs. non-peak accident counts
   - **Festival days** (Diwali, Holi, Eid, New Year) vs. non-festival accident severity
3. Cross-validated both hypotheses with three regression models, each suited to a 
   different outcome type:
   - **Logistic Regression** (target: is_fatal) — odds ratios for fatality risk
   - **Multiple Linear Regression** (target: casualties) — controls for confounding 
     factors simultaneously
   - **Poisson Regression** (target: vehicles_involved) — incident rate ratios for count data

## Key Findings
- Peak-hour timing showed no significant effect on accident counts (p = 0.406) — 
  75.26% of crashes actually occurred during off-peak hours
- Festival days showed a significant rise in casualty severity (p = 0.026), 
  confirmed as the strongest predictor in both Linear and Poisson models
- Across all three models, cause of accident (distraction, overspeeding) and 
  weekend timing remained consistently important — pointing to always-on, 
  multi-factor risk rather than a single time-window effect
- City-level clustering (Chandigarh, Chennai, Kolkata) showed distinct dominant 
  causes, suggesting interventions should be tailored per city

## Tools
Python (pandas, statsmodels), Power BI

## How to Run
Open the notebook in Google Colab or Jupyter. Requires: pandas, statsmodels, 
numpy, scipy, matplotlib/seaborn.

## Full Case Study
[Read the full write-up on my portfolio →](your-framer-link.com/projects/road-safety)
