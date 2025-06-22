# Air-Quality-Prediction
A machine learning-based analysis and prediction of air quality using environmental parameters.

# 🌫️ Air Quality and Pollution Assessment:
📄 **Dataset**: 'https://www.kaggle.com/datasets/mujtabamatin/air-quality-and-pollution-assessment/data'

This project is a data science and machine learning analysis focused on evaluating and predicting air quality based on multiple environmental factors. Using a dataset of 5000 rows , the project explores the relationship between pollutants and air quality categories and applies a classification model to predict air quality levels.


## 📂 Project Overview

- **Objective**: To assess and predict air quality levels using environmental features.
- **Tools Used**: Python, Pandas, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook
- **Model**: Logistic Regression

---

## 🧪 Dataset Details

The dataset contains 10 columns and 5000 rows. It includes the following features:

| Feature                          | Description                                |
---------------------------------|--------------------------------------------|
| `Temperature`                   | Ambient temperature                        |
| `Humidity`                      | Humidity percentage                        |
| `PM2.5`, `PM10`                 | Particulate matter concentrations          |
| `NO2`, `SO2`, `CO`              | Key pollutants (Nitrogen Dioxide, etc.)    |
| `Proximity_to_Industrial_Areas`| Distance to nearest industrial zone        |
| `Population_Density`           | Area population density                    |
| `Air Quality`                  | Target variable (Good, Moderate, etc.)     |

# To show the categories of Categorical variable:    
Air Quality: quality of air, categorized into levels such as Good, Moderate, Poor, and 
Hazardous  (Y variable) 
 
# To show the categories of Continues variable: 
1. PM2.5: particulate matter smaller than 2.5 micrometers in the air  
2. PM10: particulate matter smaller than 10 micrometers in the air 
3. NO2 (Nitrogen Dioxide): Concentration of NO2 in the air 
4. SO2 (Sulfur Dioxide): Concentration of SO2 in the air 
5. CO (Carbon Monoxide):  Concentration CO in the air 
6. Temperature: Ambient atmospheric temperature the time of measurement 
7. Humidity: Percentage of humidity in the air 
8. Population Density: The number of people per s q /km 
9. Proximity to Industrial Areas: Whether the location is near an industrial area (e.g., 
Yes/No) but here is in numerical format.


## Target Variable: Air Quality Levels
Good: Clean air with low pollution levels.
Moderate: Acceptable air quality but with some pollutants present.
Poor: Noticeable pollution that may cause health issues for sensitive groups.
Hazardous: Highly polluted air posing serious health risks to the population.

---

## 📊 Exploratory Data Analysis (EDA)
**Air Quality Distribution**
**Box plot**
**Population Density vs Proximity to Industrial Areas**

Visualized feature distributions and outliers using histograms and box plots.
Count plots to analyze category-wise air quality distribution.
Correlation heatmaps to understand inter-feature relationships.

---

## ⚙️ Data Preprocessing
Checked for null values (none found).
Converted categorical target `Air Quality` into numeric labels using `LabelEncoder`.
Scaled features using `StandardScaler`.
Split the dataset into training and testing sets (70% / 30%).

---

## 🤖 Machine Learning Model
A **Logistic Regression** model was implemented to classify air quality levels.
Logistic Regression is a supervised learning algorithm used for classification tasks. 
Simple and easy to implement L2 Regularization (Ridge Regression) Penalizes large 
coefficients to prevent overfitting. 
70% Training Data and 30% Testing Data 
Training Set: Used to train the logistic regression model. 
Testing Set: Used to evaluate model performance.
  
# Standrise the freature
Standard Scaler normalizes the dataset by making the mean = 0 and standard deviation = 1.  
It helps improve model performance, especially for algorithms that rely on distance-based on calculations.
 
# Train the Logistic Regression Model 
Penalty= ‘L2 ‘: L2 regularization (Ridge Regression) to prevent overfitting. 
C= 0.1: Controls the strength of regularization  
Model. Fit (X _ train, y _ train): Trains the model using training data 

# Evalute the model performance ###
Accuracy _score (y _ train, y _ train _ p red): Measures   the model performs on training data. 
 
Accuracy _ score (y _test, y_ test _ p red): Measures model accuracy on   test data.  
 
The gap is prevented only (~ 1.67) which the model Suggest not getting overfitting and well Generatised.

### ✅ Model Performance:
- **Training Accuracy**: 94%
- **Testing Accuracy**: 93%
- **overall Accuracy**:93.2%

### 📈 Classification Report:
```
              precision    recall  f1-score   support

           0       0.99      1.00      1.00       618
           1       0.88      0.78      0.83       148
           2       0.94      0.94      0.94       452
           3       0.82      0.85      0.83       282

    Accuracy                           0.93      1500
