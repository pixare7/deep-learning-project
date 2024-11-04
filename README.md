# Alphabet Soup Deep Learning

## Overview

Alphabet Soup, a nonprofit foundation, seeks a tool to help it identify applicants most likely to succeed if granted funding. Using a deep neural network, a binary classifier was developed to predict the likelihood of applicant success. The dataset, provided by Alphabet Soup’s business team, includes historical records of 34,000 organizations funded by the foundation. This machine learning project involved three key stages: data preprocessing, model compilation and training, and model optimization.

## Table of Contents
1. [Overview](#overview)
2. [Results](#results)
3. [Summary](#summary)
4. [Future Work](#future-work)

## Results

### Data Preprocessing

- **Target Variable**: The target variable for the model is `IS_SUCCESSFUL`, which indicates whether an applicant succeeded after receiving funding.
- **Features**: The features used in the model include `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`.
- **Removed Variables**: `EIN` and `NAME` were removed from the input data, as they are identifiers and not relevant features for prediction.

### Compiling, Training, and Evaluating the Model

- **Model Architecture**: The neural network was designed with 100 neurons distributed across 2-3 hidden layers to capture complex patterns in the data. This architecture helps balance the model’s complexity to avoid both underfitting and overfitting.
  - **Activation Functions**: ReLU activation was used for the hidden layers to introduce non-linearity and promote efficient training, while the sigmoid activation was used in the output layer, allowing for probability-based binary classification.
- **Performance**: The model's accuracy goal of 75% was not achieved; the highest accuracy reached was approximately 73%.
- **Optimization Attempts**: To improve performance, several modifications were made:
  - Dropped the `SPECIAL_CONSIDERATIONS` column.
  - Added a third hidden layer (starting from two hidden layers).
  - Increased the number of neurons in the hidden layers.
  - Reduced epochs from 100 to 80.
  
  Despite these adjustments, the accuracy remained stable at around 72%.

### Figure 1: Model Training and Evaluation Results
![Figure 1](https://github.com/pixare7/deep-learning-project/blob/main/images/fig1.png)

## Summary

The deep learning model achieved a highest accuracy of almost 73%, falling short of the target 75% accuracy. Given the importance of selecting successful applicants, a higher accuracy rate may be necessary for practical use. A different approach, such as a Random Forest classifier or a Support Vector Machine (SVM), could be tested to see if these models yield better predictive accuracy, as they may handle this dataset’s features more effectively. Additionally, oversampling or other techniques could help improve performance by addressing any class imbalance.

## Future Work

Further efforts to enhance model performance could include:
- Testing alternative machine learning algorithms, such as ensemble methods.
- Conducting feature engineering to create or transform variables that may be more predictive.
- Adjusting for potential class imbalance to improve the model's ability to correctly identify successful applicants.
