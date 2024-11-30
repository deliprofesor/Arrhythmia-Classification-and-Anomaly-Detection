# Arrhythmia-Classification-and-Anomaly-Detection

This project involves the classification of arrhythmias (heart rhythm disorders) and anomaly detection using various machine learning and deep learning techniques.

## Data Loading and Exploration:

The dataset was loaded from a CSV file titled "INCART 2-lead Arrhythmia Database.csv." The general structure of the data was explored using data.info(), data.describe(), and data.head(). Missing values and basic statistical information were checked.

## Data Visualization:

- **Distribution of Rhythm Types:** The distribution of rhythm types was visualized using sns.countplot.
- **Distribution of R-R Intervals:** The distribution of previous and subsequent R-R intervals was visualized using sns.histplot.
- **Distribution of R-Peak Values:** The distribution of R-peak values across different rhythm types was visualized using sns.boxplot.
  
## Feature Engineering:

New features were created:

- **R-R Interval Difference (RR_diff):** The difference between the previous and subsequent R-R intervals was calculated.
- **Average R-R Interval (RR_avg):** The average of the previous and subsequent R-R intervals was calculated.
- **R to P Peak Ratio (R_P_Ratio):** The ratio of R peak to P peak values was calculated.
- **T to R Peak Ratio (T_R_Ratio):** The ratio of T peak to R peak values was calculated.
  
## Correlation Matrix:
The relationships between selected features were visualized using a correlation matrix with sns.heatmap. This helped identify which features were strongly correlated with each other.

## Clustering - KMeans:
KMeans clustering was applied to the data. The number of clusters was set to 3 (n_clusters=3), and the clustering results were visualized using a scatter plot. The clusters were based on the selected features.

## Classification:

- **Data Preparation:** Features (X) and target variable (rhythm type, y) were selected, and the data was split into training and test sets.
- **Random Forest Model:** The Random Forest model was optimized using GridSearchCV for hyperparameter tuning.
- **Model Evaluation:** The model's performance was evaluated using accuracy, precision, recall, and F1 score. Additionally, the ROC curve and AUC were calculated to assess model performance.
- **Confusion Matrix:** The relationship between actual and predicted classes was visualized using a confusion matrix.
  
## Anomaly Detection:

Anomaly detection was performed using the IsolationForest algorithm. Anomalies were visualized with different colors to distinguish normal and anomalous data points.

## Deep Learning - LSTM:

The data was standardized, and the labels were encoded as categorical values. A deep learning model based on Long Short-Term Memory (LSTM) was built and trained using model.fit. The model's performance was evaluated using accuracy.

## Results and Visualization:

The training and validation loss were visualized using matplotlib and seaborn, and the results were analyzed in detail.

This project combines both data analysis and the application of machine learning and deep learning models to create a comprehensive solution for arrhythmia classification and anomaly detection.
