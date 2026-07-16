# IBM Telco Customer Churn

> **How can a telecommunications company identify customers at risk of leaving and prioritize retention efforts before churn occurs?**

---

## Project Overview

Customer churn is a major challenge for subscription-based businesses. When companies cannot identify which customers are likely to leave, retention campaigns become reactive, expensive and difficult to prioritize.

This project develops an end-to-end Machine Learning solution using the **IBM Telco Customer Churn dataset**. The analysis goes beyond predicting churn: it translates model outputs into customer risk segments, business insights and actionable retention recommendations supported by Tableau dashboards.

The final solution includes:

- Data cleaning and exploratory analysis
- Feature engineering and preprocessing
- Comparison of multiple classification models
- Class imbalance treatment using SMOTE
- Customer-level churn probabilities and risk bands
- Tableau-ready datasets for business reporting

---

## Project Highlights

- Analyzed **{TOTAL_CUSTOMERS:,} telecom customers** and their service, contract and billing behavior.
- Built and compared **Logistic Regression, Decision Tree and Random Forest** models.
- Selected **{selected_model_name}** as the final business model.
- Achieved **{selected_recall:.1%} recall**, identifying approximately three out of four customers who churned in the test set.
- Segmented customers into **Low, Medium, High and Very High** churn-risk groups.
- Exported customer predictions, model metrics and feature importance for Tableau.
- Translated model results into practical customer-retention recommendations.

---

## Business Problem

A telecommunications company wants to reduce customer churn, but retention teams cannot contact every customer.

The company needs to answer three questions:

1. **Which customers are most likely to leave?**
2. **What characteristics are associated with higher churn risk?**
3. **Which customers should the retention team prioritize?**

A useful solution must do more than maximize overall accuracy. It should identify as many potential churners as possible while providing clear customer segments for targeted intervention.

---

## Project Objectives

- Predict whether a customer is likely to churn.
- Compare different classification algorithms.
- Prioritize recall to reduce missed churners.
- Identify the strongest drivers of customer churn.
- Generate customer-level risk scores.
- Design business-oriented Tableau dashboards.
- Recommend practical retention strategies.

---

## Dataset

| Dataset characteristic | Value |
|---|---:|
| Customers | {TOTAL_CUSTOMERS:,} |
| Original variables | {ORIGINAL_VARIABLES} |
| Target variable | `churn` |
| Problem type | Binary classification |
| Positive class | Customer churned |
| Churn proportion | Approximately {actual_churn_rate:.1%} |

---

## Project Workflow

```text
Raw IBM Telco Data
        |
        v
Data Cleaning and Validation
        |
        v
Exploratory Data Analysis
        |
        v
Feature Engineering
        |
        v
Encoding and Scaling
        |
        v
Train-Test Split
        |
        v
Model Training and Tuning
        |
        v
SMOTE on Training Data
        |
        v
Model Evaluation and Selection
        |
        v
Customer Risk Segmentation
        |
        v
Tableau Dashboard and Business Recommendations
```

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   └── clean/
├── notebooks/
│   ├── 01_telco_churn_data_preparation.ipynb
│   ├── 02_feature_engineering_preprocessing.ipynb
│   ├── 03_modeling_and_tableau_export.ipynb
│   └── 04_generate_readme.ipynb
├── tableau_exports/
│   ├── tableau_customer_predictions.csv
│   ├── tableau_feature_importance.csv
│   └── tableau_model_metrics.csv
├── figures/
├── models/
├── reports/
├── requirements.txt
└── README.md
```

---

## Model Evaluation

{metrics_table}

---

## Final Model Selection

### {selected_model_name}

The final model was selected based on the business objective rather than accuracy alone.

For customer retention, a false negative represents a customer who is likely to leave but is not identified for intervention. Missing this customer may result in lost recurring revenue.

The selected model achieved:

- Accuracy: **{selected_accuracy:.1%}**
- Precision: **{selected_precision:.1%}**
- Recall: **{selected_recall:.1%}**
- F1-score: **{selected_f1:.1%}**
- ROC-AUC: **{selected_roc_auc:.1%}**

This trade-off can be acceptable when the cost of contacting an additional customer is lower than the cost of losing a customer without intervention.

---

## Test-Set Prediction Results

The final Tableau export contains **{test_customers:,} test-set customers**.

| Prediction outcome | Customers |
|---|---:|
| True Negative | {true_negative:,} |
| True Positive | {true_positive:,} |
| False Positive | {false_positive:,} |
| False Negative | {false_negative:,} |

---

## Customer Risk Segmentation

| Risk band | Customers |
|---|---:|
| Very High | {very_high_risk:,} |
| High | {high_risk:,} |
| Medium | {medium_risk:,} |
| Low | {low_risk:,} |

This segmentation makes the model operationally useful by helping retention teams prioritize customers with the highest predicted churn probability.

---

## Key Churn Drivers

{features_table}

> Feature importance indicates how useful a variable was to the model. It does not prove that the feature causes churn.

---

## Business Insights

### Contract type is strongly connected to churn risk

Month-to-month contracts are among the strongest predictors of churn. Customers with limited contractual commitment should receive targeted retention attention.

### Early-stage customers require closer monitoring

Tenure and the first 12 months of the customer relationship are important predictors. This suggests that onboarding and early customer experience are critical retention moments.

### Fiber-optic customers deserve deeper investigation

Fiber-optic service is highly influential in churn prediction. The company should investigate pricing, service quality, technical issues and customer expectations.

### Support and security services may influence loyalty

Online security and technical support appear among relevant features. Service adoption may help distinguish lower-risk and higher-risk customers.

---

## Business Recommendations

1. Prioritize Very High and High risk customers.
2. Strengthen onboarding during the first 12 months.
3. Encourage month-to-month customers to adopt longer contracts.
4. Investigate the fiber-optic customer experience.
5. Personalize offers based on risk, tenure, contract and service profile.
6. Measure retention campaigns through controlled experiments.

---

## Tableau Dashboards

The project exports three datasets:

- `tableau_model_metrics.csv`
- `tableau_customer_predictions.csv`
- `tableau_feature_importance.csv`


### Dashboard 1 — Churn Risk Overview

- Total customers analyzed
- Actual churn rate
- Customers at High or Very High risk
- Risk-band distribution
- Churn probability by contract and tenure
- High-risk customer profiles

### Dashboard 2 — Model Performance

- Model comparison
- Accuracy, Precision, Recall, F1-score and ROC-AUC
- Confusion matrix
- Before and after SMOTE
- Feature importance



---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook
- Tableau
- Git
- GitHub

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Data Preprocessing
- Binary Classification
- Hyperparameter Tuning
- Class Imbalance Treatment
- Model Evaluation
- Predictive Analytics
- Customer Segmentation
- Tableau Data Preparation
- Business Storytelling
- Git and GitHub Collaboration

---

## How to Run the Project

```bash
git clone {REPOSITORY_URL}
cd {REPOSITORY_NAME}
pip install -r requirements.txt
```

Run the notebooks in order:

1. `01_telco_churn_data_preparation.ipynb`
2. `02_feature_engineering_preprocessing.ipynb`
3. `03_modeling_and_tableau_export.ipynb`
4. `04_generate_readme.ipynb`

---

## Limitations

- The dataset does not include complaints, customer support history or satisfaction scores.
- The analysis uses a public dataset rather than a live production environment.
- Feature importance should not be interpreted as causal evidence.
- SMOTE creates synthetic training observations.
- Probability thresholds may require adjustment based on business costs.
- Model performance should be monitored over time.

---

## Future Improvements

- Test Gradient Boosting, XGBoost or LightGBM.
- Optimize the prediction threshold using business costs.
- Add SHAP values for customer-level explanations.
- Include complaints and satisfaction data.
- Measure retention uplift through A/B testing.
- Estimate customer lifetime value and revenue at risk.
- Deploy the model through Streamlit or FastAPI.

---

## Authors

- **Estefanía Baarosa** — [LinkedIn]({www.linkedin.com/in/estefaniabr})  | [GitHub]({github.com/estefaniabarrosa})
- **Romina Gutierrez** — [LinkedIn]({www.linkedin.com/in/rominadigitalpaidmedia}) | [GitHub]({github.com/romsx111})

---

## Acknowledgements

- IBM Telco Customer Churn dataset
- Ironhack Data Analytics Bootcamp

---

## License

This project is intended for educational purposes.
