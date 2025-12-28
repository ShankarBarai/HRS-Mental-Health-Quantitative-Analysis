# Social and Health Determinants of Depressive Symptoms in Older Adults
### A Quantitative Analysis of the RAND HRS Wave 15 Dataset (N=14,637)

## 📌 Project Overview
This research investigates the socioeconomic and health-related predictors of mental distress in the aging U.S. population. Utilizing a large-scale sample from the **University of Michigan’s Health and Retirement Study (HRS)**, I developed a multivariate OLS regression model to quantify the impact of education, physical health, and demographic factors on depression scores.

## 🛠️ Technical Stack
* **Language:** Python
* **Libraries:** `Pandas`, `NumPy`, `Statsmodels`, `Matplotlib`, `Seaborn`.
* **Model:** Multivariate Ordinary Least Squares (OLS) Regression.

## 📈 Key Research Findings (Statistical Summary)
The model explains 18% of the variance in depressive symptoms ($R^2 = 0.180, F(5, 14631) = 643.3, p < 0.000$). 

| Variable | Coefficient ($\beta$) | P-Value | Interpretation |
| :--- | :--- | :--- | :--- |
| **Physical Health** (`r15shlt`) | **0.7347** | **0.000** | Strongest predictor; poorer health significantly increases depression risk. |
| **Education** (`raeduc`) | **-0.0691** | **0.000** | Higher education acts as a significant protective factor. |
| **Gender** (`ragender`) | **0.2880** | **0.000** | Significant gender-based differences in reported symptoms. |
| **Age** (`r15agey_e`) | **-0.0179** | **0.000** | A slight decrease in symptoms observed with advancing age in this cohort. |
| **Marital Status** (`r15mstat`) | **0.0972** | **0.000** | Social standing/marital status significantly impacts mental well-being. |

## 🔍 Visual Diagnostics

### 1. Feature Correlation Heatmap
![Correlation Heatmap](Images/Correlation_Heatmap.png)

*This heatmap confirms the relationships between features and ensures that multicollinearity does not compromise the regression estimates.*

**Interpretation:**
* **Multicollinearity Check:** The low-to-moderate correlations between independent variables ensure the stability of the coefficients.
* **Primary Driver:** The visualization supports the regression finding that physical health has the most direct linear relationship with the CES-D 8 score.

### 2. Model Validation (Actual vs. Predicted)
![Actual vs Predicted](Images/Actual_vs_Predicted_Plot.png)

*The plot shows the distribution of model predictions against actual clinical scores, highlighting the model's reliability across the 0-8 scale.*

**Interpretation:**
* **Trend Alignment:** The clustering along the central axis demonstrates that the model effectively captures the upward trend of depressive symptoms as health and socioeconomic stressors increase.
* **Clinical Insight:** While the model is highly accurate at predicting lower-range symptoms($0-3$), the variance at higher scores ($8.0$) suggests that severe depression is influenced by complex factors beyond the primary socioeconomic variables included here.
