# Capital Bikeshare Demand Analysis
**Author:** Eric A. Frederic, MBA  
**Tools:** Python | Pandas | NumPy | scikit-learn | Plotly | Statsmodels | Jupyter Notebook  
**Repository:** capital-bikeshare-demand-analysis

---

# Business Problem

Capital Bikeshare must anticipate fluctuations in daily bicycle demand to ensure sufficient bicycle availability, optimize station capacity, and support operational planning. Understanding how weather, seasonality, holidays, and calendar effects influence ridership enables more efficient resource allocation and improves the customer experience.

This project develops an interpretable predictive model that identifies the primary drivers of daily ridership while providing actionable insights for operational decision-making.

---

# Objectives

This analysis was designed to answer several key business questions:

- Which factors have the greatest influence on daily bicycle demand?
- How do weather conditions affect ridership?
- Are there meaningful seasonal trends in usage?
- How accurately can daily demand be predicted using historical data?
- Which variables should operations managers prioritize when planning fleet allocation?

---

# Dataset

The analysis uses the **Capital Bikeshare Daily Ridership** dataset, which contains historical observations of daily bicycle rentals together with weather and calendar information.

Key variables include:

| Category | Variables |
|-----------|-----------|
| Weather | Temperature, Feels Like Temperature, Humidity, Wind Speed, Weather Conditions |
| Calendar | Month, Year, Weekday, Holiday |
| Ridership | Casual Riders, Registered Riders, Total Daily Rentals |

Additional engineered features were created during the analysis to improve interpretability and support model development.

---

# Project Workflow

The notebook follows a complete business analytics workflow:

1. Business Problem Definition
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Target Leakage Assessment
5. Linear Regression Modeling
6. Model Diagnostics
7. Multicollinearity Analysis (VIF)
8. Model Refinement
9. Business Recommendations
10. Limitations and Future Improvements

---

# Methodology

The project uses multiple linear regression to model total daily bicycle demand.

Major analytical techniques include:

- Exploratory Data Analysis
- Feature Engineering
- One-Hot Encoding of Categorical Variables
- Train/Test Split
- Multiple Linear Regression
- Residual Analysis
- Variance Inflation Factor (VIF)
- Model Comparison
- Coefficient Interpretation

Particular attention is given to avoiding target leakage and diagnosing multicollinearity to ensure the resulting model is both statistically sound and practically interpretable.

---

# Key Findings

## Model Performance

The final regression model explains approximately **81% of the variation in daily bicycle demand (R² ≈ 0.81)** while maintaining strong predictive accuracy on unseen data.

## Weather Drives Demand

Temperature and weather conditions are among the strongest predictors of daily ridership, confirming that environmental conditions substantially influence bicycle usage.
<img width="490" height="359" alt="image" src="https://github.com/user-attachments/assets/aa400277-104a-4c34-9b6b-9f606f837662" />

## Seasonality Matters

Demand varies considerably across seasons and months, demonstrating predictable cyclical patterns that can support operational planning.

## Multicollinearity Was Successfully Addressed

Exploratory diagnostics revealed severe multicollinearity between **Temperature** and **Feels Like Temperature**.

After removing the redundant predictor, the reduced model maintained nearly identical predictive performance while producing substantially more stable coefficient estimates.

---

# Business Recommendations

Based on the analysis, Capital Bikeshare could:

- Use weather forecasts to proactively redistribute bicycles across stations.
- Schedule maintenance during predictable seasonal demand slowdowns.
- Develop separate engagement strategies for casual and registered riders.
- Incorporate demand forecasts into staffing and inventory planning.
- Continue monitoring long-term ridership growth to guide infrastructure expansion.

---

# Limitations

| Limitation | Notes |
|------------|-------|
| Historical dataset | Model performance depends on historical patterns and may not fully capture future behavioral changes. |
| Daily aggregation | Station-level demand and hourly usage patterns are not modeled. |
| External factors | Events, tourism, transit disruptions, and economic conditions are not included. |
| Linear model | More complex machine learning models may improve predictive accuracy at the expense of interpretability. |

---

# Technical Details

| Component | Detail |
|----------|--------|
| Language | Python |
| Environment | Jupyter Notebook |
| Libraries | Pandas, NumPy, Plotly, scikit-learn, Statsmodels |
| Model | Multiple Linear Regression |
| Diagnostics | Residual Analysis, VIF, Model Comparison |
| Evaluation Metrics | R², MAE, RMSE |

---

# Tools Used

- Python
- Pandas
- NumPy
- Plotly
- scikit-learn
- Statsmodels
- Jupyter Notebook

---

# Background

This project was developed as a portfolio case study to demonstrate an end-to-end business analytics workflow using Python. Rather than focusing solely on predictive accuracy, the analysis emphasizes model interpretability, statistical diagnostics, and translating analytical findings into practical business recommendations. The approach reflects the type of structured, decision-oriented analysis commonly performed by Business Analysts and Data Analysts.
