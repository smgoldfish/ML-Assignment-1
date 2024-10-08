# Machine Learning Project

## Team : Alpha (07)
202418005 Anandita Saolapurkar</br>
202418015 Deepanshi Acharya</br>
202418021 Jay Deshpande</br>
202418043 Chandan Pandit

</br>

## Project Overview
This project aims to develop a regression model capable of accurately predicting flight prices. The dataset, sourced from Kaggle, contains information on various flight attributes, including:

- **Airline:** The name of the airline.
- **Flight:** The flight number.
- **Source_city:** The city of departure.
- **Departure:** The departure time.
- **Stops:** The number of stops.
- **Arrival:** The arrival time.
- **Destination_city:** The city of arrival.
- **Class:** The class of travel.
- **Duration:** The flight duration.
- **Days_left:** The number of days remaining before the flight.
- **Price:** The price of the flight.

To understand the data and identify potential relationships between variables, we conducted exploratory data analysis (EDA). This involved visualizing the data through various plots, such as bar graph, scatter plot and line graph. Additionally, we calculated correlation coefficients and used the Variance Inflation Factor (VIF) to assess multicollinearity among the features.

After exploring the data, we experimented with different regression models, including linear regression, random forest and knn regression. These models were evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Mean Absolute Percentage Error (MAPE), and R-squared. Based on the evaluation results, we selected the random forest regressor as the most effective model for predicting flight prices.

#### Dataset Source
https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction/data 
</br></br>

## Psuedocode for chosen model
Among the considered models, Random Forest regressor emerged as the top choice based on the previously mentioned evaluation metrics. Following is the psuedocode for the same:

```
1. Initialize the Random Forest Regressor
   - Set the number of trees (n_estimators)
   - Set other hyperparameters (depth, min_samples_split, min_samples_leaf)

2. For each tree in the forest:
   a. Sample with replacement from the training data to create a bootstrap sample
   b. Train a decision tree regressor on the bootstrap sample
      - At each node, randomly select a subset of features
      - Split the node based on the best feature from the subset
      - Repeat until the stopping criteria are met (depth, min_samples_split, min_samples_leaf)

3. To make a prediction for a new instance:
   a. Pass the instance through each tree in the forest
   b. Collect the predictions from all trees
   c. Average the predictions to get the final output
```

</br>

## Practical Applications
A few real world cases where this model can be deployed are:</br>

1. **Airlines:** To optimize pricing strategies, maximize revenue, and better anticipate demand.
2. **Corporations:** To develop effective travel policies, allocate flight allowances, and control travel costs.
3. **Travel Agencies:** To offer more accurate pricing and create personalized travel packages.
4. **Insurance Companies:** To underwrite travel insurance policies more effectively, assess risk accurately, and provide tailored coverage.

</br>

## Conclusion
Our project successfully developed a Random Forest regression model capable of accurately predicting flight prices. The model achieved an R-squared score of 97.02%, indicating that it can explain a significant portion of the variance in flight prices. This performance surpasses the results obtained from the other tested models, linear regression and KNN.

The accompanying table demonstrates the model's effectiveness in predicting flight prices across a range of scenarios:
| Actual | Predicted |
|-------|-------|
| 4721 | 4703.828902 |
| 3999 | 4034.865126 |
| 64173 | 62483.070938 |
| 5873 | 4596.781099 |
| 7212 | 6631.559051 |
