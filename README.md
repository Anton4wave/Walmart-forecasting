# Walmart sales forecasting
There are many seasons that sales are significantly higher or lower than averages. If the company does not know about these seasons, it can lose too much money. Predicting future sales is one of the most crucial plans for a company. Sales forecasting gives an idea to the company for arranging stocks, calculating revenue, and deciding to make a new investment. Another advantage of knowing future sales is that achieving predetermined targets from the beginning of the seasons can have a positive effect on stock prices and investors' perceptions. Also, not reaching the projected target could significantly damage stock prices, conversely. And, it will be a big problem especially for Walmart as a big company.

This dataset was taken from the Kaggle website. 

My goal in this project is to do an accurate data analysis, build a model that predicts store sales. With this model, Walmart authorities can determine their plans for the future, which is very important for allocating inventory, calculating revenue, and deciding whether to make new investments or not.


## Content
- [technologies](#technologies)
- [EDA](#EDA)
- [Prediction](#Prediction)

## Technologies
- Pandas
- Matplotlib
- Seaborn
- Sklearn
- Xgboost
- Grid Search
- SARIMAX
- ARIMA
- Exponential Smoothing 


## EDA
Average Monthly Sales

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/b3e07597-b6ad-42e6-aa82-3722af47bfa7)

Average Year Sales

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/cf226b81-bad3-437f-97a3-9e1ff4106045)

The impact of holidays on sales

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/64aa7e79-98ce-4ea6-bcc1-f50ba5bacb49)

Effect of Temperature

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/e9dc97fc-722e-4ce3-b41f-f236c570f2c1)


A couple of conclusions can be drawn:

- Firstly, the number of sales depends greatly on the month

- Secondly, Walmart's sales are falling every year

- Thirdly, according to statistics, there are more sales during the weekend

## Time Series Analysis

График распределения еженедельных продаж и скользящее среднее 

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/e2763b2d-69d7-46d9-9af9-82590ad5fcfb)


## Prediction 

Metrics for this competition: The metric of the competition is weighted mean absolute error (WMAE). Weight of the error changes when it is holiday.

![image](https://github.com/Anton4wave/Walmart-forecasting/assets/100091790/174b5c63-27ee-45c3-bf17-e1a97a9a40d0)

Modeling:

- For the baseline I used RandomForestRegressor and get WMAE = 6691

- Then I removed unnecessary columns and trained the model again, obtaining WMAE = 4215

- Then I used XGBoost. WMAE = 3096

- Then I used XGBoost and RandomForestRegressor with KFold - got the best value. WMAE = 2188

