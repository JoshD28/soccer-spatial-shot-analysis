# Soccer Spatial Shot Analysis (WSL 2020/21)

This repository contains a course lab using **StatsBomb Open Data** (FA Women’s Super League 2020/2021) to build and evaluate a **shot difficulty model (Expected Goals, xG)** and visualize spatial scoring probability across the pitch.

## Lab Goals
1. **Create a Shot Difficulty Model (Expected Goals)** using **logistic regression** on StatsBomb Open Data (WSL 2020/21).
2. **Rank the Top 10 players** by **cumulative expected goals (xG)** across the season.
3. **Evaluate the model** using appropriate diagnostics and performance metrics.
4. **Plot a probability surface** using `mplsoccer` to show the spatial distribution of scoring probability across the field.

## Methods Overview
- **Data source:** StatsBomb Open Data (FA WSL 2020/21)
- **Model:** Logistic Regression (goal vs. no-goal outcome)
- **Key features (typical):** shot distance, shot angle, body part, play type (depending on availability in the notebook)
- **Diagnostics (examples):** ROC-AUC, confusion matrix, calibration/reliability, residuals (as implemented in the notebook)
- **Visualization:** spatial binning of xG values and a contour-based probability surface on a StatsBomb pitch

## Outputs
- **xG model** (logistic regression) and summary of coefficients/interpretation
- **Top 10 player table** by cumulative xG (season total)
- **Model evaluation plots/metrics**
- **Pitch probability surface** showing estimated scoring probability by location

## How to Run
1. Clone/download this repository.
2. Open the notebook:
   - `Shot_Difficulty_Model_for_Soccer.ipynb`
3. Run cells top-to-bottom.

## Requirements
- Python 3.x
- pandas, numpy, matplotlib
- scikit-learn
- mplsoccer

## Notes
This lab focuses on **expected goals as a measure of shot difficulty**, not player finishing ability. Player ranking is based on **cumulative xG**, which reflects shot quantity and shot quality over the season.
