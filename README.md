# Breast Cancer Prediction Using Machine Learning and Deep Learning

## Project Overview

This project focuses on predicting whether a breast tumor is **benign or malignant** using two approaches: a **logistic regression model** and a **deep learning neural network**. The goal is to explore how a classic, interpretable method compares with a modern deep learning model in terms of accuracy and generalization when applied to a real-world medical dataset.

The dataset used is the **Breast Cancer Wisconsin (Diagnostic)** dataset, which includes 30 numerical features derived from digitized images of fine needle aspirates (FNA) of breast masses.

---

## Exploratory Data Analysis (EDA)

- Checked for missing values and confirmed the dataset was clean.
- Analyzed distributions of features using histograms and boxplots.
- Investigated relationships between variables using correlation heatmaps.
- Identified key contributing features to target prediction based on correlation.

---

## Data Preprocessing

- Standardized numerical features using **StandardScaler** for both models.
- Converted target labels from strings (`M`, `B`) to binary integers (`1`, `0`).
- Split the data into **training** and **testing** sets (typically 80/20).
- For deep learning:
  - Converted labels to one-hot encoding.
  - Applied batch normalization in the model to stabilize training.

---

## Models Implemented

### 1. **Logistic Regression**

- Used as the baseline model for binary classification.
- Evaluated using accuracy, confusion matrix, precision, recall, and F1-score.
- **Model Performance:**
  - High accuracy on both training and test data.
  - Provides good interpretability for feature impact.

### 2. **Deep Neural Network (DNN)**

- Implemented using **Keras** with the following architecture:
  - Input layer with 30 features
  - Two hidden layers with ReLU activation
  - Dropout for regularization
  - Output layer with sigmoid activation
- Used **binary crossentropy** loss and **Adam optimizer**.
- **Model Performance:**
  - Accuracy on par or slightly better than logistic regression.
  - Better at capturing subtle non-linear relationships in data.

---

## Evaluation Metrics

- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report** (Precision, Recall, F1)
- **Loss and Accuracy Plots** (for DNN model)

---

## Model Performance Summary

| Model              | Accuracy (Test) | Notes                          |
|-------------------|------------------|--------------------------------|
| Logistic Regression | ~96%            | Simple, fast, highly interpretable |
| Deep Neural Network | ~97–98%         | Slightly better generalization, more complex |

- Logistic Regression performed very well considering its simplicity.
- DNN offered marginal improvement, with better performance on some edge cases.
- Both models are viable for deployment depending on requirements.

---

## Conclusion

This project demonstrated that both logistic regression and deep learning models are effective for breast cancer prediction using the given dataset. While logistic regression provides transparency and simplicity, deep learning may offer slight performance gains, especially when extended with further feature engineering or larger datasets.
