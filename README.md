# Diabete_Analysis

Multiple Linear Regression Project
Yanda Lyu | University of San Francisco

Overview
This project analyzes the diabetes.txt dataset (366 subjects, 16 variables) to identify significant predictors of glyhb (glycosylated hemoglobin) levels—an indicator for diabetes diagnosis. All analysis is performed in R with full code and outputs provided.

Workflow
Data Exploration

Identify and classify variables as quantitative or qualitative.

Visualize distributions (histograms, pie charts).

Analyze pairwise relationships (scatterplot matrix, correlation matrix).

Full Model Fitting

Regress glyhb on all predictors.

Assess model assumptions with diagnostic plots.

Transformation

Use Box-Cox to determine optimal transformation for glyhb.

Refit model using transformed response and check diagnostics.

Data Splitting

Set random seed (372), split into 70% training and 30% test sets.

Model Selection: First-Order Effects

Run all subsets regression (regsubsets from leaps).

Evaluate models by SSE, R², adjusted R², Cp, AIC, BIC.

Identify best models by AIC (Model 3.1), BIC (Model 3.2), and adjusted R² (Model 3.3).

Model Selection: Main Effects + Interactions

Fit full model with all main effects and two-way interactions.

Apply ridge and LASSO regression (glmnet), using cross-validation for λ selection.

Compare models and report selected predictors.

Model Validation

Internal: Calculate PRESS for each selected model.

External: Compute MSPE on the test set for each model.

Compare internal and external validation results to select the final model.

Final Model

Fit final selected model to the full dataset.

Report summary and interpret results in context.
