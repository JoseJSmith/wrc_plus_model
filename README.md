# wRC+ Prediction Model  
**Predicting Player Performance with Statcast + FanGraphs Data**

[![View on GitHub](https://img.shields.io/badge/GitHub-View%20Repo-black?logo=github)](https://github.com/JoseJSmith/wrc_plus_model)

---

## Overview

This project builds a predictive model for **Weighted Runs Created Plus (wRC+)**, one of the most advanced metrics in modern baseball analytics. Using Statcast and FanGraphs data from the 2023–2024 seasons, we attempt to model offensive output by leveraging underlying batted ball profiles, quality of contact, and expected statistics.

While the initial model is built using basic regression and Random Forest, the framework can be extended with more advanced techniques (e.g., XGBoost, Ridge/Lasso, Neural Nets) in the future.

---

## Files in This Repo

- `wRC+_Prediction_Model.ipynb`: The main notebook with data cleaning, modeling, and evaluation.
- `2024_fangraphs-leaderboards.csv`: FanGraphs advanced metrics for 2024.
- `2024_exit_velocity.csv`: Statcast batted ball data for 2024.
- `2023_exit_velocity.csv`: Statcast data from 2023 for comparison or future use.

---

## Current Modeling Results

| Model Type            | R² Score | RMSE   |
|-----------------------|----------|--------|
| **Baseline Mean Model** | 0.100    | 22.70  |
| **Multivariable Linear Regression** | 0.024    | 23.64  |
| **Random Forest Regressor**         | -0.171   | 25.89  |

➡ So far, the **baseline mean model performs the best**. There's room to improve with better feature selection and model tuning.

---

##  Next Steps

- Expand feature engineering (e.g., percentile rankings, max EV, xwOBA, pull%).
- Try advanced models like **XGBoost** or **ElasticNet**.
- Incorporate plate discipline metrics (e.g., O-Swing%, BB%, K%) for better context.
- Add visualizations to communicate results interactively.
- Deploy as a Streamlit app for team-level projections.

---

##  Learnings

- Even high-quality metrics like **exit velocity** or **barrel%** don’t fully capture offensive value in isolation.
- **Combining multiple sources** (Statcast + FanGraphs) adds depth but requires clean merging and careful feature selection.
- **Overfitting** is a concern — especially with small sample sizes or correlated features.

---

##  Connect With Me

**Jose Smith**  
🔗 GitHub: [@JoseJSmith](https://github.com/JoseJSmith)

---


