# Whoop Recovery Score Prediction Project

## Project Overview

This project focuses on predicting fatigue based on resting heart rate (RHR) data collected over 10 consecutive months. The dataset is part of a personal fitness analysis using data from the Whoop fitness tracker. By analyzing the RHR data, the goal is to develop a model that can predict fatigue levels, helping to optimize rest and performance.

---

## Dataset

The dataset includes daily RHR measurements spanning 10 months, providing valuable insights into recovery and fatigue patterns. Key features in the dataset are:

- **Date**: The date of each measurement.
- **Resting Heart Rate (RHR)**: Measured in beats per minute (bpm).
- **Sleep Debt**: The difference between actual and required sleep.
- **Recovery Score**: An overall measure of physical recovery.

---

## Project Workflow

### **1. Data Cleaning and Preparation**

- Removed any missing or duplicate values from the dataset.
- Converted date values to a consistent datetime format for easier analysis.
- Normalized numerical columns for better compatibility with machine learning models.
- Split the dataset into training and testing sets.

### **2. Exploratory Data Analysis (EDA)**

#### Key Visualizations:

- **Yearly Trend of RHR (2024)**:
  ![Yearly RHR](https://github.com/charlesdaigre/PROJECT_WHOOP/blob/main/RHR_2024.png)
  
  This graph shows the RHR trend throughout 2024, highlighting fluctuations due to varying levels of physical activity and recovery.

- **Correlation: Sleep Debt vs. RHR**:
  ![Sleep Debt vs. RHR](https://github.com/charlesdaigre/PROJECT_WHOOP/blob/main/correlation_RHR_SLEPTDEPT.png)
  
  This scatterplot indicates how sleep debt impacts RHR, revealing significant patterns.

- **Correlation Matrix**:
  ![Correlation Matrix](https://github.com/charlesdaigre/PROJECT_WHOOP/blob/main/matrix.png)
  
  The heatmap highlights relationships between key variables such as RHR, sleep debt, and recovery score.

- **Correlation: Recovery Score vs. RHR**:
  ![Recovery Score vs. RHR](https://github.com/charlesdaigre/PROJECT_WHOOP/blob/main/rcovery_score_RHR.png)
  
  This visualization demonstrates the link between recovery score and RHR, showing inverse correlation trends.

### **3. Feature Engineering**

- Created new features to enhance predictive power:
  - **7-Day RHR Average**: Captures weekly trends.
  - **Sleep Debt Recovery Ratio**: Quantifies recovery improvements based on sleep debt.

### **4. Fatigue Prediction Model**

- **Model Selection**: Evaluated several machine learning models, including:
  - Linear Regression
  - Random Forest Regressor
  - Gradient Boosting Regressor
- **Final Model**: Gradient Boosting Regressor achieved the best performance.
- **Evaluation Metrics**:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

#### Prediction Results Visualization:
![Prediction Results](https://github.com/charlesdaigre/PROJECT_WHOOP/blob/main/prediction_recovery.png)

This graph compares actual vs. predicted fatigue levels, demonstrating the model’s accuracy.

---

## Key Insights and Recommendations

1. **Resting Heart Rate Trends**: Monitoring RHR trends helps identify periods of high fatigue, signaling the need for increased recovery efforts.
2. **Impact of Sleep Debt**: Consistently reducing sleep debt improves RHR and recovery scores.
3. **Optimized Rest Periods**: Incorporating regular rest based on predicted fatigue levels can enhance overall performance.

---

## Tools and Technologies

- **Python**: Used for data analysis, cleaning, and modeling.
- **Pandas**: For data manipulation.
- **Matplotlib & Seaborn**: For creating visualizations.
- **Scikit-learn**: For building and evaluating machine learning models.
- **Jupyter Notebooks**: Documented the entire process with interactive outputs.

---

## Conclusion

This project highlights how data from wearable devices can be leveraged to gain actionable insights into recovery and fatigue management. The developed fatigue prediction model provides a foundation for optimizing physical performance and recovery strategies. Future improvements could include integrating additional metrics such as workout intensity or heart rate variability.

