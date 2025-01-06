# Car Evaluation Classification using K-Nearest Neighbors (KNN)

## Overview

This project uses a **K-Nearest Neighbors (KNN)** classifier to predict the **Condition** of a car based on several features such as **Buying**, **Maint**, **Doors**, **Persons**, **Lug_boot**, and **Safety**. The dataset consists of categorical variables, and the goal is to evaluate the condition of the car, which can be one of the following:

- **unacc**: Unacceptable
- **acc**: Acceptable
- **vgood**: Very Good
- **good**: Good

To address class imbalance issues in the dataset, **SMOTE (Synthetic Minority Over-sampling Technique)** is applied to balance the class distribution by generating synthetic samples for the minority classes.

## Dataset

The dataset consists of the following columns:

- **Buying**: The buying price of the car (`vhigh`, `high`, `med`, `low`)
- **Maint**: The maintenance cost of the car (`vhigh`, `high`, `med`, `low`)
- **Doors**: The number of doors in the car (`2`, `3`, `4`, `5more`)
- **Persons**: The number of persons the car can carry (`2`, `4`, `more`)
- **Lug_boot**: The size of the car's luggage boot (`small`, `med`, `big`)
- **Safety**: The safety level of the car (`low`, `med`, `high`)
- **Condition**: The target variable, representing the car's condition (`unacc`, `acc`, `vgood`, `good`)

## Steps

1. **Data Preprocessing**:
   - The dataset was cleaned and categorical variables were encoded using **Ordinal Encoding**.
   - **SMOTE** was applied to oversample the minority classes.

2. **Model Building**:
   - The **K-Nearest Neighbors (KNN)** algorithm was used for classification.
   - The model was trained on the resampled dataset.

3. **Model Evaluation**:
   - The model was evaluated using the **classification report** containing metrics like **precision**, **recall**, **f1-score**, and **accuracy**.
   - A **confusion matrix** was used to visualize the performance of the classifier.

## Installation

To run this project, you need to have Python installed. You can set up the project by installing the required libraries:

```bash
pip install -r requirements.txt
