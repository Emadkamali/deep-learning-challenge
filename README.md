---

## Overview of the Analysis

The primary objective of this analysis is to develop a robust deep learning model to predict the success of charity donation applications using the provided dataset. This involves multiple phases, including data cleaning, feature engineering, model construction, training, and optimization, aiming to achieve an accuracy target of 75%.

## Results

### Data Preprocessing

**Target Variable**:
  - IS_SUCCESSFUL: Indicates whether a charity donation application was successful.
  
- **Feature Variables**: 
  - `APPLICATION_TYPE`
  - `AFFILIATION`
  - `CLASSIFICATION`
  - `USE_CASE`
  - `ORGANIZATION`
  - `STATUS`
  - `INCOME_AMT`
  - `SPECIAL_CONSIDERATIONS`

- **Removed Variables**:
-   EIN, NAME, and ASK_AMT: These columns were excluded from the analysis as they serve as identifiers and do not contribute predictive value to the model.

### Compiling, Training, and Evaluating the Model

**Neurons, Layers, and Activation Functions**:
 **First Model**:
  **First hidden layer**: 80 neurons, ReLU activation
  **Second hidden layer**: 30 neurons, ReLU activation
  **Output layer**: 1 neuron, sigmoid activation

**Second Model**:
  **First hidden layer**: 85 neurons, ReLU activation
  **Second hidden layer**: 30 neurons, sigmoid activation
  **Output layer**: 1 neuron, sigmoid activation
  
**Third Model**:
  **First hidden layer**: 100 neurons, ReLU activation
  **Second hidden layer**: 50 neurons, ReLU activation
  **Output layer**: 1 neuron, sigmoid activation

These configurations were selected after experimenting with various neuron counts and activation functions to identify the optimal model architecture. ReLU activations were used in hidden layers to mitigate the vanishing gradient issue, while the sigmoid function was employed in the output layer for binary classification, providing a probability score.

**Model Performance**:
  The goal was to achieve a 75% accuracy on the test data. Although this exact target was not consistently met, the model's hyperparameters, including the number of neurons, layers, and activation functions, were iteratively fine-tuned to maximize performance.

**Steps to Increase Model Performance**:
  **Data Scaling**: StandardScaler was applied to normalize the feature data.
  **Categorical Encoding**: One-hot encoding was used to convert categorical variables into a numerical format suitable for training.
  **Model Architecture Tuning**: Various neuron and layer configurations were tested.
  **Training Epochs**: The model was trained for 100 epochs to ensure adequate learning time.
  **Optimization Techniques**: Different optimization algorithms and learning rates were experimented with.

Summary

The deep learning model demonstrated its capability to predict the success of charity donation applications. However, achieving the exact target accuracy of 75% remained a challenge. The model's architecture, including the number of neurons, layers, and activation functions, was optimized through iterative experimentation.


**Recommendations for Further Enhancement**:
  **Ensemble Methods**: Combining multiple models, such as Random Forest and Gradient Boosting, could potentially capture more complex patterns in the data.
  **Hyperparameter Tuning**: Employ grid search or randomized search to systematically fine-tune hyperparameters.
  **Feature Engineering**: Investigate additional techniques to derive more informative features from the existing data.
  **Cross-Validation**: Implement cross-validation to ensure the model's performance is robust and generalizes well to unseen data.
  
Exploring these strategies may lead to improved accuracy and reliability in predicting the success of charity donation applications.
