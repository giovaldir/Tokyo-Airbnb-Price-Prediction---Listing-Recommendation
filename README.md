# Tokyo Airbnb Price Prediction & Listing Recommendation
- dataset : http://insideairbnb.com/


![](tokyo-wallpaper.jpg)


# Business Understanding
## Problem Statement

In recent years, the popularity of Airbnb accommodations has grown rapidly, and Tokyo, being one of the most vibrant and culturally rich cities in the world, attracts millions of tourists annually. However, for travelers and property owners alike, accurately predicting the price of an Airbnb listing and recommending suitable spaces for guests can be challenging due to various factors that influence pricing and user preferences.

The objective of this Data Science project titled "Tokyo Airbnb Price Prediction & Listing Recommendation" is to develop a comprehensive model that can predict the price of Airbnb listings in Tokyo accurately. Additionally, the project aims to provide personalized recommendations for spaces that align with guests' preferences and requirements.

## Goals

- Accurate Price Prediction: Develop a reliable Tokyo Airbnb price prediction model to aid hosts in setting optimal listing prices and maximizing revenue.
- Enhanced User Experience: Build a personalized recommendation system that suggests suitable Airbnb spaces to travelers based on their preferences, improving user satisfaction.
- Market Insights: Gain valuable insights into key factors influencing Airbnb prices in Tokyo to inform property management and investment decisions.

## Steps
The key steps in the "Tokyo Airbnb Price Prediction" project include:

- Data Understanding:
Collect relevant data from Airbnb sources, including listing details, descriptions, amenities, review scores, and historical booking data.
Explore and analyze the collected data to understand its structure, quality, and potential issues.
Identify data types, missing values, outliers, and patterns within the dataset.
- Data Preparation:
Cleanse and preprocess the data by handling missing values, outliers, and inconsistencies.
Perform feature engineering to create informative features from available data, such as sentiment analysis of reviews and text analysis of descriptions.
Prepare the data for modeling by encoding categorical variables, scaling numerical features, and splitting the dataset into training and testing sets.
- Modeling:
Select appropriate regression algorithms for price prediction, such as Linear Regression, Random Forest, XGBoost, and Support Vector Regression (SVR).
Train and tune the selected models using the training dataset.
Evaluate model performance using appropriate evaluation metrics like Mean Squared Error (MSE), R-squared, and Root Mean Squared Error (RMSE).
- Evaluation:
Compare the performance of different regression models to identify the most accurate and reliable model for price prediction.
Validate the model's ability to generalize by evaluating its performance on the testing dataset.
Assess the model's prediction accuracy against the project's objectives and business requirements.
- Deployment:
Deploy the selected price prediction model to a web-based platform to make it accessible to users.
Develop a user interface that allows users to input listing features and receive predicted rental prices.
Ensure the deployed model's reliability, scalability, and responsiveness.

## Dataset

![](https://github.com/giovaldir/Predicting-Airbnb-Prices-using-Regression/blob/d5ba15952c9324d480b2b9a71e5b24993659ff8a/Screenshot%20(1488).png)

### Method
- Price Prediction

Regression Algorithms: Different regression algorithms are used for price prediction, including Linear Regression, Random Forest, XGBoost, and SVR. These algorithms learn patterns from historical data to predict rental prices.

Model Evaluation: Models are evaluated using various metrics such as Mean Squared Error (MSE), R-squared, and Root Mean Squared Error (RMSE). These metrics measure the accuracy and goodness of fit of the model's predictions.

- Listing Recommendation

Cosine Similarity: For the recommendation system, a content-based approach is used. Cosine similarity is calculated between different listings based on features such as listing descriptions, amenities, and review scores.

User Preferences: User preferences and historical booking data are used to personalize recommendations. Listings with higher cosine similarity scores are recommended based on their similarity to the user's preferences.

# Data Understanding
Gather data from various sources, including Airbnb listings, geospatial datasets, user reviews, and property amenities information. Explore the data to gain insights into its structure, quality, and potential issues that need to be addressed during data cleaning and preprocessing.

Listing Dataset

![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/f888445ddeed29b49e8c679da793947c4f8f23de/Screenshot%20(2322).png)

Calendar Dataset

![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/f888445ddeed29b49e8c679da793947c4f8f23de/Screenshot%20(2323).png)

Review Dataset

![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/f888445ddeed29b49e8c679da793947c4f8f23de/Screenshot%20(2324).png)

Numerical

![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/b69aba019a52a642cd1021d2e1ac5730742600d9/histograms%20(1).jpg)

Categorical

![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/b69aba019a52a642cd1021d2e1ac5730742600d9/countplots%20(1).jpg)

Map
![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/acbca16c0a420dc25b2874ca4fc82c3c14ead790/Screenshot%20(2325).png)


# Data Preparation
- Data Cleaning:

Handling Missing Values: Identify columns with missing values and decide how to handle them. Depending on the significance and amount of missing data, you might choose to impute missing values with mean, median, mode, or a more advanced technique like regression imputation or using external data sources.

Outlier Detection: Identify outliers that could negatively impact model performance. Outliers can be detected using statistical methods, visualization, or domain knowledge. Decide whether to remove, transform, or keep outliers based on their impact on the analysis.

- Feature Engineering:

Creating New Features: Generate new features that provide additional insights into the data. For example, you could create a feature representing the number of available amenities in a listing or calculate the ratio of positive to total reviews as a sentiment feature.

Feature Scaling: Normalize numerical features to bring them to a similar scale. Common techniques include min-max scaling or z-score normalization. This ensures that features with different scales do not dominate the modeling process.

- Handling Categorical Data:

Encoding Categorical Variables: Convert categorical variables into numerical format that machine learning algorithms can understand. Common methods include one-hot encoding, label encoding, and target encoding. Each method has its advantages based on the nature of the data and the algorithm used.

- Splitting the Dataset:

Training and Testing Sets: Divide the dataset into training and testing sets. The training set is used to train the machine learning models, while the testing set is used to evaluate their performance. A common split ratio is 70-30 or 80-20.

# Modeling and Evaluation

|       Model       |     MSE Train      |      MSE Test      |    R^2 Train     |    R^2 Test     |
|-------------------|--------------------|--------------------|------------------|-----------------|
| Linear Regression |  1.850886e+07      |  1.811550e+07      |  0.395847        |  0.411155       |
| Random Forest     |  5.623683e+03      |  3.936338e+04      |  0.999816        |  0.998720       |
| XGBoost           |  1.204195e+05      |  1.800360e+05      |  0.996069        |  0.994148       |
| SVR               |  3.480605e+07      |  3.510720e+07      | -0.136114        | -0.141162       |

Linear Regression:
- The linear regression model achieved an MSE (Mean Squared Error) of approximately 1.85e+07 on the training data and 1.81e+07 on the test data.
- The R-squared value, denoted as R^2, indicates that around 39.6% of the variance in the target variable can be explained by the model's predictions on the training data, and about 41.1% on the test data.

Random Forest:
- The random forest model demonstrated strong performance with significantly lower MSE values of 5.62e+03 on the training data and 3.94e+04 on the test data.
- The high R^2 values close to 1 indicate that the model fits the training data exceptionally well (99.98%), and it generalizes effectively to the test data (99.87%).

XGBoost:
- The XGBoost model performed well with an MSE of approximately 1.20e+05 on the training data and 1.80e+05 on the test data.
- The R^2 values, close to 1, suggest that the XGBoost model captures the underlying patterns in the training data (99.61%) and maintains strong generalization to the test data (99.41%).

SVR (Support Vector Regression):
- The SVR model yielded higher MSE values, indicating less accurate predictions, with MSE values of 3.48e+07 on the training data and 3.51e+07 on the test data.
- The negative R^2 values (-0.14) suggest that the SVR model is not a good fit for the data, as it performs worse than a horizontal line representing the mean of the target variable.

In summary, the random forest and XGBoost models outperformed the linear regression and SVR models in terms of prediction accuracy, with strong R^2 values and lower MSE values. These models are better suited for capturing the complex relationships in the dataset, leading to more accurate price predictions and listing recommendations in the context of Tokyo Airbnb listings.

# Listing Recommendation

The process of providing listing recommendations by looking at Airbnb listings that have a review score rating of >90 in the most profitable areas/neighborhoods. The target of this recommendation is established Airbnb entrepreneurs who have been in business but have not been profitable enough. By providing this recommendation, the established Airbnb entrepreneur will know what the market likes, what specifications are actually needed for their Airbnb in that neighborhood, and of course, it will make it easier for the entrepreneur to improve their previous failures.


![](https://github.com/giovaldir/Tokyo-Airbnb-Price-Prediction---Listing-Recommendation/blob/b69aba019a52a642cd1021d2e1ac5730742600d9/Recommendation%20System.png)

### Thank You
