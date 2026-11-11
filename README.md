# Customer Churn Prediction

## Project Overview

This project aims to investigate customer churn using exploratory data analysis (EDA), statistical methods, and machine learning. The goal is to identify patterns associated with customer cancellation and, in later stages, develop and evaluate predictive models.

The project is being developed incrementally using Python and Google Colab, with version control through Git and GitHub.

**Current status:** Exploratory Data Analysis (EDA) and statistical analysis.

## Objectives

- Explore customer characteristics and churn distribution.
- Identify patterns and associations between customer attributes and churn.
- Apply statistical tests to investigate relationships between categorical variables.
- Prepare a reproducible dataset for machine learning.
- Develop and evaluate baseline classification models.
- Translate model results into interpretable findings relevant to customer retention.

## Dataset

- **Source:** Kaggle.
- **Size:** 5,000 customer records.
- **Target variable:** `churned`.
  - `0`: Customer did not churn.
  - `1`: Customer churned.
- **Access method:** The dataset is accessed directly from Kaggle through Google Colab.

The dataset's exact name, source URL, license, and feature definitions should be documented once verified.

## Technology Stack

- Python
- Pandas
- NumPy
- Matplotlib and Seaborn
- SciPy
- Google Colab
- Git and GitHub

## Exploratory Data Analysis

The current EDA includes:

- Target variable inspection and churn distribution.
- Numerical feature distributions and histograms.
- Categorical feature frequency analysis.
- Churn analysis by inactivity period.
- Contingency tables and statistical analysis of categorical variables.

### Preliminary Findings

**Customer inactivity**

The analysis identified a positive association between `last_login_days` and churn. Churn rates also vary across inactivity groups. These findings require further investigation, particularly to ensure that the features would be available at the intended prediction time.

**Subscription type and churn**

A Chi-square test of independence was applied to investigate the association between `subscription_type` and `churned`.

| Statistic | Result |
|---|---:|
| Chi-square statistic | 133.2778 |
| Degrees of freedom | 2 |
| Cramér's V | 0.1633 |

The Chi-square test indicated a statistically significant association between subscription type and churn. Cramér's V suggests that the association is relatively weak.

These results indicate statistical association, not causation or guaranteed predictive performance.

## Current Stage

The project is currently focused on EDA and statistical foundations. No final predictive model or validated model performance is being claimed at this stage.

## Next Steps

1. Complete churn-rate analysis across categorical features.
2. Investigate numerical features and data quality.
3. Review statistical assumptions and document feature associations.
4. Assess potential data leakage, especially in inactivity-related variables.
5. Prepare the modeling dataset and feature preprocessing pipeline.
6. Define the validation strategy and evaluation metrics.
7. Train a baseline Logistic Regression model.
8. Compare alternative classification algorithms.
9. Interpret model results and assess their potential business relevance.
10. Document the final MVP and its limitations.

## Repository Structure

```text
customer-churn-prediction/
├── notebooks/
│   └── 01_eda.ipynb
├── README.md
└── .gitignore
```

Additional folders and files will be introduced as the project evolves.

## Reproducibility

The current analysis is performed in Google Colab. To reproduce the work:

1. Open the notebook in `notebooks/`.
2. Access the dataset from its verified Kaggle source.
3. Configure any required Kaggle authentication securely, if applicable.
4. Run the notebook cells in sequence.

Dataset access instructions, dependency versions, and the exact source reference will be documented as the project progresses.

## Limitations

- Findings are preliminary and depend on the available dataset.
- Statistical association does not establish causation.
- Feature usefulness must be assessed within a valid prediction setup.
- Model performance, generalization, and business impact have not yet been established.

## License and Data Usage

The repository's license and the dataset's redistribution terms have not yet been verified. Dataset usage and licensing conditions should be reviewed before redistribution.

## Project Status

**In progress — EDA and statistical analysis.**
