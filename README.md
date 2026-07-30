# 🌧️ Rain Prediction in Australia: Machine Learning Classification

## 📌 Project Overview
This project applies machine learning classification algorithms to predict whether it will rain tomorrow in various locations across Australia. By analyzing historical weather data, we built and compared multiple models to find the most accurate predictor.

## 📊 Exploratory Data Analysis (EDA)
We explored the relationships between numerical features to understand dependencies and avoid multicollinearity. 
![Correlation Heatmap](images/correlationi_heatmap.png)

To better understand the distributions and detect outliers in our continuous variables, we visualized the numerical features:

**Feature Distributions (Histograms):**
Visualizing the distributions of features like Rainfall, Evaporation, and Wind Speeds reveals right-skewed patterns.
![Histograms](images/histogram_of_data.png)

**Outlier Detection (Boxplots):**
Boxplots highlight the presence of extreme values in our weather data that require specific handling before modeling.
![Boxplots](images/box_plot_of_data.png)

## 🛠️ Data Preprocessing & Feature Engineering

To enhance model reliability and ensure a robust evaluation process, a comprehensive preprocessing pipeline was developed. The following steps were applied:

* **Outlier Detection & Treatment:**  
  Extreme weather values were handled using a **capping (winsorization) approach** rather than removal, preserving valuable information while reducing the impact of potential anomalies.

* **Missing Data Handling:**  
  Missing values were carefully processed through separate imputation strategies for **numerical and categorical features**, maintaining data consistency and preventing information loss.

* **Feature Scaling & Normalization:**  
  Numerical features were standardized using **StandardScaler** to achieve comparable feature distributions and improve the performance of distance-based and gradient-based machine learning algorithms.

* **Data Splitting Strategy:**  
  The dataset was divided into training and testing sets using an **85/15 split ratio**, ensuring an unbiased evaluation of the model's generalization capability on unseen weather data.

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

---
### Performance of Other Evaluated Models

#### Logistic Regression (Threshold = 0.35)
**Confusion Matrix:**
![Logistic Regression CM](images/Losgistic_threshold_consuion_matrix.png)

**ROC Curve (AUC = 0.873):**
![Logistic Regression ROC](images/Logistic_threshold_ROC.png)

#### Decision Tree
**Confusion Matrix:**
![Decision Tree CM](images/decision_tree_confusion_matrix.png)

**ROC Curve (AUC = 0.844):**
![Decision Tree ROC](images/ROC_curve_decision_tree.png)

#### Gaussian Naive Bayes
**Confusion Matrix:**
![Naive Bayes CM](images/NP_confusion_matrix.png)

**ROC Curve (AUC = 0.75):**
![Naive Bayes ROC](images/NP_ROC.png)

## 👥 Team Members

* **Youssef Mahmoud** - [LinkedIn Profile](https://www.linkedin.com/in/youssef-mahmoud-3a633225b/)
* **[Name of the second member]** - [LinkedIn Profile](حط لينك LinkedIn هنا)
* **[Name of the third member]** - [LinkedIn Profile](حط لينك LinkedIn هنا)
* * **[Name of the fourth member]** - [LinkedIn Profile](حط لينك LinkedIn هنا)
