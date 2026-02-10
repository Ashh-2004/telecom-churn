# # Telecom Customer Churn Analysis & Predictive Modeling

## ## Project Overview

This project addresses the high cost of customer attrition in the telecommunications industry. Using a dataset of **7,043 customers**, I conducted a full-stack data science workflow—from rigorous statistical testing to deploying a high-performance machine learning model—to identify high-risk customers before they leave.

## ## Key Business Questions Answered

* **Price vs. Satisfaction:** Is churn driven by expensive bills or poor experience? (Answer: Satisfaction is the primary driver).
* **The Onboarding Gap:** Do new customers churn more than long-term ones? (Answer: Yes, the first 12 months are high-risk).
* **Contractual Impact:** Does moving customers to long-term contracts actually reduce churn? (Answer: Yes, 2-year contracts reduce churn rate by over 40%).

---

## ## Technical Deep Dive

### ### 1. Statistical Validation

Instead of relying on visual intuition alone, I used:

* **Independent T-Tests:** To prove that differences in `monthly_charges` and `tenure` between churned and retained customers were statistically significant ().
* **Chi-Square Test of Independence:** To validate the relationship between `contract_type` and `churn_label`.

### ### 2. Machine Learning Pipeline

I implemented a **Random Forest Classifier** optimized for high-imbalanced data.

* **Handling Imbalance:** Utilized `class_weight="balanced"` to ensure high sensitivity to churners.
* **Performance Metric:** Focused on **ROC-AUC (0.96)** and **Recall (0.90)** to minimize "False Negatives" (missing a customer who is about to leave).
* **Feature Importance:** Identified `satisfaction_score`, `number_of_referrals`, and `contract_type` as the top three predictors.

---

## ## Key Results

* **Model Accuracy:** 88%
* **ROC-AUC:** 0.96 (Excellent predictive separation)
* **Top Insight:** Churned customers have an average satisfaction score of **1.7**, compared to **3.8** for loyal customers. Retention efforts should focus on "Experience Recovery" rather than just "Price Discounts."

## ## Technologies Used

* **Language:** Python
* **Libraries:** `pandas`, `seaborn`, `matplotlib`, `scikit-learn`, `scipy`
* **Environment:** Jupyter Notebook / Anaconda

---

## ## How to Run

1. Clone this repository.
2. Install requirements: `pip install pandas matplotlib seaborn scikit-learn scipy kagglehub`.
3. Run `churn.ipynb`. Note: The notebook automatically downloads the dataset via `kagglehub`.

---

**Would you like me to also write a 2-sentence "Impact Statement" for your LinkedIn profile to go along with this?**
