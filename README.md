# 🌧️ Rain Prediction in Australia: Machine Learning Classification

## 📌 Project Overview
This project applies machine learning classification algorithms to predict whether it will rain tomorrow in various locations across Australia. By analyzing historical weather data, we built and compared multiple models to find the most accurate predictor.

## 📊 Exploratory Data Analysis (EDA)
We explored the relationships between numerical features to understand dependencies and avoid multicollinearity. 
![Correlation Heatmap](images/correlationi_heatmap.png)

## 🛠️ Data Preprocessing & Cleaning
To ensure high model performance and prevent data leakage, the following robust preprocessing pipeline was implemented:
* **Train-Test Split:** Data was split initially (85% Train, 15% Test) to ensure completely unbiased evaluation.
* **Handling Outliers:** Applied **Capping** instead of dropping for extreme weather values to preserve dataset integrity.
* **Missing Values Imputation:** Handled numerical and categorical missing data separately using rigorous strategies.
* **Feature Scaling:** Applied `StandardScaler` to normalize features for distance-sensitive algorithms.

## 🤖 Models Trained
We experimented with four different classification models to establish the best decision boundary:
1. **Logistic Regression** 
2. **Decision Tree** 
3. **Random Forest** 
4. **Gaussian Naive Bayes**

## 📈 Results & Best Model Performance
*(Here is the performance summary of our trained models on the unseen test set)*

| Model | Accuracy |
| :--- | :---: |
| **Random Forest** | **85%** |
| Logistic Regression | 84% |
| Decision Tree | 78% |
| Naive Bayes | 65% |

*(Note: Accuracy percentages in the table can be manually updated in this README to reflect the exact decimals from the notebook).*

### Best Model Performance (Random Forest)
Below is the Confusion Matrix and ROC Curve for our top-performing model:

**Confusion Matrix:**
![Confusion Matrix](images/Random_forest_consuion_matrix.png)

**ROC Curve:**
![ROC Curve](images/ROC_curve_random_forest.png)
