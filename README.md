# Predicting Successful Funding Applications for Alphabet Soup

---

## Introduction

### Purpose of the Analysis

The purpose of this analysis is to develop a binary classifier using neural networks that can predict the success of funding applications for Alphabet Soup. The goal is to identify features that are most indicative of a successful application, thereby helping Alphabet Soup allocate their resources more effectively.

## Data Preprocessing

### Data Overview

The dataset contains metadata about over 34,000 organizations that have received funding from Alphabet Soup. Key features include:

- **EIN and NAME**: Identification columns
- **APPLICATION_TYPE**: Alphabet Soup application type
- **AFFILIATION**: Affiliated sector of industry
- **CLASSIFICATION**: Government organization classification
- **USE_CASE**: Use case for funding
- **ORGANIZATION**: Organization type
- **STATUS**: Active status
- **INCOME_AMT**: Income classification
- **SPECIAL_CONSIDERATIONS**: Special considerations for application
- **ASK_AMT**: Funding amount requested
- **IS_SUCCESSFUL**: Was the money used effectively (target variable)

### Data Cleaning and Preprocessing Steps

1. **Dropped non-beneficial columns**: `EIN` and `NAME`
2. **Encoded categorical variables** using one-hot encoding
3. **Normalized numerical variables** using StandardScaler

## Model Development

### Initial Model

An initial neural network model was developed with the following structure:

- Input Layer: Features after preprocessing
- Hidden Layers: Two dense layers with ReLU activation
- Output Layer: Single neuron with sigmoid activation

### Optimized Model

The model was optimized by:

- Adding additional hidden layers
- Modifying the number of neurons in each layer
- Using different activation functions
- Adjusting the learning rate

## Results

### Questions Answered

1. **What variable(s) are considered the target(s) for your model?**
   - The target variable is `IS_SUCCESSFUL`.

2. **What variable(s) are the features for your model?**
   - All other columns after dropping `EIN` and `NAME` and preprocessing (encoding and scaling).

3. **What preprocessing steps were taken?**
   - Dropped non-beneficial columns, encoded categorical variables, normalized numerical variables.

4. **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
   - The initial model used two hidden layers with ReLU activation, and the output layer used sigmoid activation. The number of neurons and layers were determined based on the complexity of the dataset and the need to balance bias and variance.

5. **Were you able to achieve the target model performance?**
   - Yes, the optimized model showed improved performance metrics compared to the initial model. Specific metrics such as accuracy, precision, recall, and F1-score were used to evaluate performance.

6. **What steps did you take to try and increase model performance?**
   - Added additional hidden layers, varied the number of neurons, experimented with different activation functions, and adjusted learning rates.

## Summary of Results

The final neural network model showed a significant improvement over the initial model. Key performance metrics indicated that the model is capable of effectively predicting the success of funding applications.

## Alternative Models

Other machine learning models, such as Random Forest, Gradient Boosting, or Support Vector Machines, could also be used to solve this problem. These models might offer better performance for certain types of datasets or be more interpretable. For example, a Random Forest model can handle non-linear relationships and interactions between features well and provides feature importance scores, which can be useful for understanding the impact of each feature.

## Conclusion

The neural network model developed in this analysis provides a robust tool for Alphabet Soup to predict the success of funding applications. By leveraging the insights from this model, Alphabet Soup can make more informed decisions, ultimately leading to more effective use of their funds.

