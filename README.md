# Machine Learning Project

## Team : Alpha (07)
202418005 Anandita Saolapurkar</br>
202418015 Deepanshi Acharya</br>
202418021 Jay Deshpande</br>
202418043 Chandan Pandit


## Project Overview
In this project, we aim to build a regression model to predict  CO<sub>2</sub> emissions from vehicles based on various attributes. A dataset which provides detailed information on vehicle characteristics like engine size, cylinder count, and fuel consumption was sourced from Kaggle. An effort has been made to explore the relationship between these attributes and the CO<sub>2</sub> emissions.

To achieve this, we implemented four regression models: Ridge, Random Forest, Decision Tree and Linear Regression. Each model is trained to predict the CO<sub>2</sub> emissions, and their performance is evaluated using multiple metrics like MAPE, MSE, MAE and R<sup>2</sup>.

#### Dataset Source
https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction/data


## Psuedocode for chosen model
Among the considered models, Random Forest regressor emerged as the top choice based on the previously mentioned evaluation metrics. Following is the psuedocode for the same:

```
1. Initialize the Random Forest Regressor
   - Set the number of trees (n_estimators)
   - Set other hyperparameters (e.g., max_depth, min_samples_split)

2. For each tree in the forest:
   a. Sample with replacement from the training data to create a bootstrap sample
   b. Train a decision tree regressor on the bootstrap sample
      - At each node, randomly select a subset of features
      - Split the node based on the best feature from the subset
      - Repeat until the stopping criteria are met (e.g., max_depth, min_samples_split)

3. To make a prediction for a new instance:
   a. Pass the instance through each tree in the forest
   b. Collect the predictions from all trees
   c. Average the predictions to get the final output
```
