# Market Mix Modeling (MMM) Using Bayesian Inference

## Overview

This project presents an end-to-end Market Mix Modeling (MMM) pipeline to quantify the impact of marketing channels (TV, Social Media, Newspaper) on product sales. It applies traditional regression models alongside a Bayesian Log-Log regression enhanced with Adstock transformation and MCMC sampling to estimate probabilistic ROAS (Return on Ad Spend). Ultimately, the project also optimizes the marketing budget using linear programming for maximum effectiveness.

## Key Objectives

- Understand how different marketing channels contribute to sales.
- Build and compare predictive models: Linear, Ridge, Random Forest, and Bayesian Regression.
- Apply Adstock to model the carryover effect of advertising.
- Estimate ROAS with confidence intervals using Bayesian Inference.
- Optimize media spend allocation using Linear Programming.

## Features & Methodology

### Exploratory Data Analysis (EDA)

### Key Features
- Data loading and initial exploration
- Missing value analysis
- Data cleaning (removing redundant columns)
- Statistical description of features
- Duplicate value check
- Distribution analysis through histograms
- Correlation matrix visualization
- Feature relationship investigation

In short:
- Checked for duplicates, missing values, and outliers.
- Normalized non-Gaussian features using Box-Cox Transformation.
- Correlation heatmaps and pairplots to understand feature interactions.

### Modeling Approaches

- **Linear Regression**: Baseline modeling of feature influence.
- **Random Forest**: Captures non-linearity and ranks feature importance.
- **Ridge Regression**: Handles multicollinearity.
- **Bayesian Linear Regression (with PyMC)**:
  - Probabilistic model for capturing uncertainty in coefficients.
  - Used MCMC sampling to generate posterior distributions.

### Adstock Transformation

- Applied to simulate memory effect of advertising on consumers.
- Compared multiple lag values; retained most relevant configuration.

### ROAS Estimation

- ROAS computed for each channel.
- Found Social Media to be the highest-performing channel with 95% confidence.

### Budget Optimization

- Used Linear Programming to reallocate spend based on ROAS.
- Suggested reallocating approximately 70% of the budget to Social Media for optimal returns.


## Libraries Used

- `pandas`, `numpy`, `seaborn`, `matplotlib` – EDA and visualization
- `scikit-learn`, `statsmodels`, `scipy` – Modeling and diagnostics
- `PyMC` – Bayesian regression and MCMC sampling
- `PuLP` or `SciPy.optimize` – Linear programming for budget optimization

## Results & Insights

- Social Media generated the highest returns on investment.
- Bayesian modeling provided uncertainty-aware estimates via confidence intervals.
- Budget optimization led to significant potential ROAS improvement.



