# 💾 Backblaze 2013 Hard Drive Reliability Analysis

### Predicting Hard Drive Failure Using Statistical and Survival Analysis

## 📌 Project Overview

This project analyzes the reliability of 29,072 hard drives using Backblaze 2013 data. It applies statistical and machine learning techniques to understand hard-drive failure patterns, estimate survival probabilities, investigate SMART attributes, and study missing-data mechanisms.

The main objective is to understand how survival analysis and statistical modelling can help identify factors associated with hard-drive failures.

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA).
- Analyze failure patterns across different hard-drive brands.
- Estimate survival probabilities using Kaplan–Meier analysis.
- Fit Weibull survival models using Maximum Likelihood Estimation.
- Investigate latent failure patterns using Weibull Mixture Models and EM.
- Compare OLS and robust LAD regression.
- Identify failure-risk associations using Cox Proportional Hazards regression.
- Study MCAR, MAR, and MNAR missing-data mechanisms.

## 📊 Dataset Description

| Metric                |               Value |
| --------------------- | ------------------: |
| Total hard drives     |              29,072 |
| Recorded failures     |                 724 |
| Right-censored drives |              28,348 |
| Failure proportion    |               2.49% |
| Observation period    | April–December 2013 |
| Daily source files    |                 266 |

The analysis uses drive-level information, including brand, model, capacity, observed duration, failure status, and SMART attributes.

**Note:** The duration represents observed follow-up time, not the complete lifetime of a drive.

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Statsmodels
- Lifelines
- Jupyter Notebook / Google Colab

## 🔬 Methodology

### 1. Exploratory Data Analysis

- Dataset inspection and preprocessing.
- Failure and censoring distribution.
- Brand-wise failure comparison.
- SMART attribute analysis and missing-value investigation.

### 2. Survival Analysis

- Kaplan–Meier survival estimation.
- Brand-wise survival comparison.
- Log-rank hypothesis testing.
- Survival sensitivity analysis.

### 3. Weibull Modelling

- Weibull Maximum Likelihood Estimation.
- Survival and hazard function estimation.
- Bootstrap confidence intervals.
- Two-component Weibull mixture using the EM algorithm.

### 4. Robust Regression

- Ordinary Least Squares (OLS).
- Least Absolute Deviations (LAD).
- Majorization–Minimization optimization.
- Sensitivity analysis.

### 5. Cox Proportional Hazards

- Cox regression modelling.
- Hazard ratio estimation.
- Concordance evaluation.
- Schoenfeld residual diagnostics.
- Custom Newton–Raphson implementation.

### 6. Missing Data Analysis

- MCAR, MAR, and MNAR simulations.
- Mean and median imputation.
- RMSE-based comparison.

## 📈 Key Findings

- The dataset contains 724 recorded failures among 29,072 drives.
- Kaplan–Meier median survival was not reached during the observation period.
- Brand-wise survival curves showed statistically significant differences.
- Weibull shape estimate: 0.9283.
- Cox model concordance index: 0.86.
- Reallocated and pending sector measurements showed positive hazard associations.
- Proportional-hazards diagnostics identified violations for certain predictors.

## 📁 Project Structure

```text
Backblaze-Reliability-Analysis/
│
├── Backblaze_2013_Hard_Drive_Reliability_Analysis.ipynb
│
├── Backblaze_Hard_Drive_Reliability_Report.pdf
│
└── README.md
```

*The prepared drive-level CSV is required to reproduce the analysis and should be placed in the working directory.*

## ▶️ How to Run

**1. Clone the repository**

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Backblaze-Reliability-Analysis
```

**2. Install dependencies**

```bash
pip install numpy pandas matplotlib seaborn scipy scikit-learn statsmodels lifelines
```

**3. Prepare the dataset**

Place `backblaze_2013_drive_level.csv` in the appropriate working directory.

**4. Run the notebook**

Open the Jupyter Notebook or upload it to Google Colab and execute the cells sequentially.

## ⚠️ Limitations

- The observation period is limited to 2013.
- Drive installation dates are unavailable.
- SMART attributes may have manufacturer-specific encodings.
- Cox proportional-hazards assumptions are violated for some predictors.
- The custom Cox implementation does not converge within the specified iteration limit.
- Missing-data mechanism experiments use simulated data rather than actual Backblaze missingness.

## 👥 Project Team

| Name         | Roll Number |
| ------------ | ----------- |
| Rathod Akash | BSD-BG-2415 |
| Tabish       | BSD-DH-2423 |
| Sujit        | BSD-CC-2422 |

**Contribution:** Rathod Akash – End-to-end project execution.

## 🏁 Conclusion

This project demonstrates how statistical modelling and survival analysis can be used to investigate hard-drive reliability. By combining exploratory analysis, survival estimation, parametric modelling, robust regression, Cox regression, and missing-data simulations, it provides a comprehensive statistical approach to understanding hard-drive failure patterns.

---

**Project Domain:** Statistical Analysis | Reliability Engineering | Survival Analysis | Data Science
