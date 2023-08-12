## DSN Microsoft Bootcamp  Hackathon 2023

#### Data Description

Wazobia Real Estate Limited, is a prominent real estate company operating in Nigeria. With a vast portfolio of properties, they strive to provide accurate and competitive pricing for houses. However, they have been facing challenges in accurately predicting the prices of houses in the current market. To overcome this hurdle, Wazobia Real Estate Limited is seeking the expertise of data scientists like you to develop a robust predictive model.

#### Objective

The objective of this hackathon is to create a powerful and accurate predictive model that can estimate the prices of houses in Nigeria. By leveraging the provided dataset, you will analyze various factors that impact house prices, identify meaningful patterns, and build a model that can generate reliable price predictions. The goal is to provide Wazobia Real Estate Limited with an effective tool to make informed pricing decisions and enhance their competitiveness in the market.

#### Walkthrough

Here is the link to the dataset: <a href="[https://www.w3schools.com/](https://zindi.africa/competitions/free-ai-classes-in-every-city-hackathon-2023/data)">Hous prediction dataset</a>
The training dataset contains `14,000` rows and `7` columns `6` of which were predictors of the house price, the predictors include loc, parking space, bathroom, bedroom, id, and title.

#### Data Cleaning:
- Filled the bedroom and bathroom columns with the standard deviation and the parking space column with zero.
- Dropped rows that had missing values for title and loc location columns.

#### Feature Engineering:

- Manually encoded the house types by ranking them in order of the average price from the smallest to largest. 
- Created a new column labeled geopolitical zone and performed a one-hot encoding on the column as well as the loc (state) column. 
- Also created a new column labeled bedroom-to-bathroom ratio.

#### Model Building
- Used both CatBoostRegressor and LightGBM algorithm to train my model.
- To avoid overfitting and bias in my model, I employed a 10-fold cross-validation using K-fold.

#### Model Evaluation
- With RMSE as the lost function, I recorded a score of `415,958` for the LightGBM model and `415,504` for the CatBoost Model.

- I blended the result of the two models with `70%` of the CatBoost model and `30%` of the light GB model to obtain my final submission on the competition’s Leaderboard, which produced an RMSE score of `326,609` (6th place score).

#### Feature Importance:
- For the LightGBM model the top three features include title, bedroom, and bathroom while the CatBoost model's top three features were title, bedroom, and loc_encoded.




```python

```
