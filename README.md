Flood Prediction Model - Multiple Linear Regression

[Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-orange.svg)](https://scikit-learn.org/)

Project Overview

This project implements a **Multiple Linear Regression** model to predict flood probability in Nigeria using 20 environmental and infrastructural features. The model achieves exceptional predictive performance with an R² score of 1.0, demonstrating perfect alignment between predicted and actual flood probabilities.

Objectives

- Develop a robust regression model for flood risk assessment
- Identify key environmental and infrastructural factors influencing flood probability
- Demonstrate proficiency in machine learning model development, evaluation, and visualization
- Provide actionable insights for flood management and disaster preparedness

Dataset

Source: Kaggle Flood Prediction Dataset (50,000 records, 21 features)

Features Include:
1. MonsoonIntensity - Seasonal rainfall patterns
2. TopographyDrainage - Land elevation and water flow
3. RiverManagement - River control systems
4. Deforestation - Forest cover loss
5. Urbanization - Urban development index
6. ClimateChange - Climate impact indicators
7. DamsQuality - Dam infrastructure condition
8. Siltation - Sediment accumulation
9. AgriculturalPractices - Farming methods impact
10. Encroachments - Illegal development
11. IneffectiveDisasterPreparedness - Emergency readiness
12. DrainageSystems - Urban drainage quality
13. CoastalVulnerability - Coastal risk factors
14. Landslides - Land instability
15. Watersheds - Water catchment areas
16. DeterioratingInfrastructure - Aging facilities
17. PopulationScore - Population density impact
18. WetlandLoss - Wetland degradation
19. InadequatePlanning - Urban planning gaps
20. PoliticalFactors - Governance indicators
21. FloodProbability - Target variable (0-1 scale)

Methodology

Data Preprocessing
- Loaded and explored dataset using Pandas
- Performed statistical analysis and data validation
- Analyzed feature distributions and correlations

Feature Selection
- Calculated correlation coefficients for all features
- Selected top 20 features based on absolute correlation with target
- Visualized relationships using pairplots and correlation heatmaps

Model Development
- Algorithm: Multiple Linear Regression (Ordinary Least Squares)
- Train/Test Split: 80% training, 20% testing
- Random State: 42 (for reproducibility)
- Implementation: Scikit-learn LinearRegression

Evaluation Metrics
- Mean Absolute Error (MAE): Average prediction error magnitude
- Mean Squared Error (MSE): Average squared prediction error
- Root Mean Squared Error (RMSE): Standard deviation of residuals
- R-squared (R²): Proportion of variance explained by the model

Results

Model Performance

| Metric | Value |
|--------|-------|
|R-squared (R²) | 1.000 |
|Mean Absolute Error (MAE) | 9.72×10⁻¹⁶ |
|Mean Squared Error (MSE) | 1.47×10⁻³⁰ |
|Root Mean Squared Error (RMSE) | 1.21×10⁻¹⁵ |

Key Insights

Perfect Predictive Accuracy: The model achieves an R² score of 1.0, indicating perfect alignment between predicted and actual values

Top Predictive Features:
1. DeterioratingInfrastructure
2. TopographyDrainage
3. RiverManagement
4. Watersheds
5. DamsQuality

Multivariate Relationships: While individual features show modest correlations (~0.20-0.25), their combined effect produces perfect predictions.

Project Structure

flood-prediction-mlr/
├── data/
│   └── flood.csv
├── notebooks/
│   └── Multiple_Linear_Regression_Flood.ipynb
├── outputs/
│   ├── model_evaluation_metrics.csv
│   ├── model_coefficients.csv
│   ├── top_10_scatter_matrix.png
│   └── actual_vs_predicted.png
├── README.md
└── requirements.txt


Installation & Usage

Prerequisites
- Python 3.8 or higher
- pip package manager

Dependencies
1. numpy>=1.21.0
2. pandas>=1.3.0
3. matplotlib>=3.4.0
4. seaborn>=0.11.0
5. scikit-learn>=1.0.0
6. jupyter>=1.0.0

Visualizations
1. Actual vs Predicted Values
    Scatter plot demonstrating perfect alignment along the regression line, validating model accuracy.
2. Feature Correlation Analysis
    Bar chart displaying the top 10 features with highest absolute correlation to flood probability.
3. Pairplot Matrix
    Comprehensive visualization showing pairwise relationships and distributions across all features.

Analysis Notes
Why Perfect R²?
    An R² score of 1.0 is exceptionally rare in real-world datasets. Possible explanations:
        Synthetic Data: The dataset may contain mathematically generated relationships
        Deterministic Formula: Target variable might be calculated from features
        Data Leakage: Features may contain direct information about the target
        Controlled Environment: Data collected under controlled conditions

Recommendations for Future Work

    External Validation: Test model on independent, real-world flood data
    Feature Engineering: Explore non-linear relationships and interactions
    Model Comparison: Benchmark against Random Forest, XGBoost, Neural Networks
    Cross-Validation: Implement k-fold cross-validation for robustness
    Deployment: Develop API for real-time flood risk assessment

Skills Demonstrated

1. Multiple Linear Regression implementation
2. Feature selection and correlation analysis
3. Data visualization (Matplotlib, Seaborn)
4. Model evaluation and metrics interpretation
5. Statistical analysis with Pandas and NumPy
6. Machine learning workflow (train/test split, fitting, prediction)
7. Professional code documentation

Author
Obinna Nwosu C

