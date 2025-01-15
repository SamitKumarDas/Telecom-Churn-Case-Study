# Telecom Churn Case Study

## Project Overview

This project focuses on **predicting customer churn** for a telecom company using machine learning techniques. The goal is to identify customers at high risk of churn and the key factors influencing their decision, enabling the company to implement effective retention strategies.

---

## Problem Statement

In the telecom industry, customer churn poses a significant challenge. With high acquisition costs, retaining existing customers is critical. This project aims to:

1. Predict churn for high-value customers.
2. Identify key drivers of churn.
3. Provide actionable recommendations to reduce churn.

---

## Approach

### 1. **Data Understanding and Cleaning**
- Loaded and explored the dataset.
- Handled missing values by imputing or dropping columns based on relevance.
- Removed irrelevant features such as `mobile_id` and date-related columns.

### 2. **Feature Engineering**
- Created new features to capture trends in customer activity (e.g., recharge patterns, call usage).
- Tagged churners based on a usage-based definition.
- Segmented high-value customers using the 70th percentile of average recharge amounts.

### 3. **Dimensionality Reduction (PCA)**
- Reduced the dimensionality of the dataset using PCA while retaining 90% variance.
- Used transformed principal components in some models for better performance and reduced overfitting.

### 4. **Model Building and Evaluation**
- Built and evaluated multiple models, including:
  - Logistic Regression
  - Random Forest
  - XGBoost (Tuned and Weighted)
- Used metrics like accuracy, precision, recall, F1-score, and AUC-ROC for performance evaluation.

### 5. **Hyperparameter Tuning**
- Applied RandomizedSearchCV and GridSearchCV to optimize model performance.

---

## Results

| **Model**              | **Accuracy** | **Precision** | **Recall** | **F1-Score** | **AUC-ROC** |
|-------------------------|--------------|---------------|------------|--------------|-------------|
| Logistic Regression     | 91.66%       | 58.09%        | 10.22%     | 17.38%       | 87.55%      |
| Random Forest           | 94.15%       | 75.46%        | 47.35%     | 58.19%       | 91.89%      |
| Tuned XGBoost           | 94.29%       | 72.06%        | 54.72%     | 62.21%       | 93.40%      |
| Weighted XGBoost        | 91.46%       | 50.16%        | 80.47%     | 61.80%       | 93.54%      |

---

## Recommendations

1. **Proactive Engagement:**
   - Target customers with declining recharge or usage trends with personalized offers.

2. **Service Quality Improvements:**
   - Address network issues like call drops and poor connectivity in critical regions.

3. **Loyalty Programs:**
   - Offer rewards for consistent usage to high-value customers.

4. **Real-Time Monitoring:**
   - Use predictive models to flag high-risk customers and intervene promptly.

---

## How to Use

1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the repository directory:
   ```bash
   cd telecom-churn-analysis
   ```

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook "Telecom churn case study.ipynb"
   ```

4. Access the supporting files from the shared Google Drive link:
   - **Data Dictionary:** [Data Dictionary - Telecom Churn Case Study](https://drive.google.com/drive/folders/1Rw8YbgSz8JKtA1p0MTIohn_YHYCygBAl?usp=sharing)
   - **Dataset:** [Telecom Churn Dataset](https://drive.google.com/drive/folders/1Rw8YbgSz8JKtA1p0MTIohn_YHYCygBAl?usp=sharing)

5. Run the notebook step by step to explore the data and model results.

---

## Dependencies

The project requires the following Python libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

Install the dependencies using:
```bash
pip install -r requirements.txt
```

---

## Author

- **Samit Kumar Das**

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
