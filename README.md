# Sachin_project
# California Housing Price Prediction

This project uses the California Housing Prices dataset to build a linear regression model for predicting housing prices.

## Dataset

The California Housing Prices dataset contains information about median house values in Californian districts. 

The dataset has the following attributes:

- MedInc median income in block group
- HouseAge median house age in block group
- AveRooms average number of rooms per household
- AveBedrms average number of bedrooms per household
- Population total population
- AveOccup average number of household members
- Latitude block group latitude
- Longitude block group longitude

The target variable is the median house value for each district.

## Project Steps

The project involves the following steps:

1. **Data Loading:** Load the California Housing Prices dataset from scikit-learn.

2. **Data Exploration:** Analyze the dataset using descriptive statistics and visualizations to understand the data distribution, identify potential outliers, and explore relationships between variables.
    - Create a Pandas DataFrame from the dataset.
    - Display the first and last few rows of the DataFrame.
    - Add the target variable ('Price') to the DataFrame.
    - Get information about the DataFrame (data types, non-null values).
    - Calculate descriptive statistics for the DataFrame.
    - Check the size of the DataFrame (number of rows and columns).
    - Check for missing values in the DataFrame.
    - Calculate the correlation between variables.
    - Create a pairplot to visualize relationships between variables.
    - Create a boxplot to identify potential outliers.

3. **Feature Engineering:** Create new features from existing ones to potentially improve model performance.
    - Create 'RoomsPerHousehold' feature by dividing 'AveRooms' by 'AveOccup'.
    - Create 'BedroomsPerRoom' feature by dividing 'AveBedrms' by 'AveRooms'.

4. **Data Preprocessing:** Prepare the data for model training.
    - Separate the features (X) and the target variable (y).
    - Split the data into training and testing sets.
    - Scale the features using StandardScaler.
    - Visualize the scaled data using boxplots.

5. **Model Training:** Train a linear regression model on the preprocessed data.
    - Create a LinearRegression model object.
    - Fit the model to the scaled training data.
    - Print the model coefficients and intercept.

6. **Model Evaluation:** Evaluate the performance of the trained model.
    - Make predictions on the scaled testing data.
    - Calculate the residuals (difference between actual and predicted values).
    - Create a distribution plot of the residuals.
    - Calculate performance metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared score.
    - Calculate the adjusted R-squared score.

7. **Model Saving:** Save the trained model for future use.
    - Use pickle to save the model to a file named 'regmodel.pkl'.

8. **Model Loading and Prediction:** Load the saved model and make predictions.
    - Use pickle to load the saved model.
    - Make predictions on new data using the loaded model.


## Conclusion

This project demonstrates the process of building a linear regression model for predicting housing prices using the California Housing Prices dataset. The model can be further improved by exploring different feature engineering techniques, trying other regression models, or fine-tuning hyperparameters.
