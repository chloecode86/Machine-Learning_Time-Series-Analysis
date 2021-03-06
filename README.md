# Machine-Learning-Project
>### Time Series Analysis on Walmart Sales <br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/Walmart.png" width="600" height="280"> <br /> 

#### Business Objective
Mainly to analyze the Walmart sales data and predict their stores’ sales. Also, to examine if there is seasonal sales pattern which could be beneficial for better marketing strategies. The significance of several macro-indicators like CPI, Unemployment rate, Fuel price etc. , which provided from the dataset, against the sales figure have also been examined.


#### Data Collection
The dataset is obtained from Kaggle. <br /> 
<br />
df.head() <br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/df_head.png" width="680" height="180"> <br /> 

#### Methodoly
1. Data Preprocessing via EDA & data cleaning. <br /> 
2. Build models to predict the sales. <br /> 
3. Evaluate the models & compare their respective RMSE. <br /> 

#### Exploratory Data Analysis
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/EDA_Sales.png" width="650" height="280"> <br /> 
Some seasonal peak sales pattern is shown around the year-end.<br />
<br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/EDA_Variables.png" width="650" height="280"> <br /> 
Some outliers are shown in Unemployment rate.
<br /> 
#### Models Used
1. ARIMA <br /> 
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/ARIMA.png" width="500" height="300"> <br /> 

2. FB PROPHET<br /> 
Univariate <br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/FB_prophet_1.png" width="580" height="300"> <br /> 
Multivariate (add_regressor with **fuel_price** and **unemployment_rate**) <br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/FB_prophet_2.png" width="590" height="300"> <br /> 
Seasonality (with regards to **Christmas**, **Thanksgiving** and **Superbowl**)<br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/FB_prophet_3.png" width="580" height="300"> <br /> 
3. LSTM <br />
<img src="https://github.com/chloecode86/Machine-Learning-Project/blob/main/graphs/LSTM.png" width="500" height="300"> <br /> 


#### Models Evaluation
1. ARIMA <br />
   - RMSE : 5136942.16 <br />
2. FB PROPHET <br />
   - Univariate :  <br />
      - RMSE : 3852421.52 <br />
   - Multivariate : <br />
      - RMSE : 3836873.23 <br />
   - Seasonality : <br />
      - RMSE : 1970243.04 <br />
3. LSTM <br />
   - RMSE : 5097790.39 <br />
 <br />
Based on the RMSE values, we can conclude that fbProphet has given us the best results. But given that we have more data, with proper fine tuning, LSTM & ARIMA may perform better as well.

