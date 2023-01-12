# Time-Series_forecasting
Time-series forecasting using ML to predict the Indian stock market crash in March 2020. Leveraged tensorflow and keras to test MLP and LSTMs; utilized matplotlib for data visualizations

Stock market data; 75/25 train test split provided data till just prior to the crash.
<img width="720" alt="Screen Shot 2023-01-13 at 1 18 37 AM" src="https://user-images.githubusercontent.com/34772344/212166386-e44af461-613f-4b19-839c-fae5429b8e23.png">


ADF test results: (-0.7032637672443643, 0.8459023363533136, 10, 1310, {'1%': -3.4353516488758684, '5%': -2.8637488209107196, '10%': -2.5679459879960373}, -7415.090077941648)
High p-value of ADF test (0.8459023363533136) shows that we fail to reject null hypothesis. 
 Hence, the dataset is non-stationary.
<img width="810" alt="Screen Shot 2023-01-13 at 1 19 47 AM" src="https://user-images.githubusercontent.com/34772344/212166674-42d9c415-b5c1-43ce-a26c-ceba9f40334b.png">


Results after Rolling Mean
ADF test results: (-7.80780640688324, 9.004790086644209e-13, 10, 1300, {'1%': -2.5674619923076922, '5%': -1.9412085922972235, '10%': -1.6166172866800181}, -7488.189124476252)
low p-value of ADF test (3.277335734460085e-12) shows that we will reject null hypothesis. 
 Hence, the residual is close to stationary.
P-value of ADF test on the noise (with no constant no trend) shows that data is stationary.
 Hence, we can say that data is trend stationary.
<img width="341" alt="Screen Shot 2023-01-13 at 1 21 32 AM" src="https://user-images.githubusercontent.com/34772344/212167046-4fbeb811-a173-416f-a142-390dc64ecd2b.png">


Results after first difference
ADF test results: (-10.871160694174854, 1.3357913098839414e-19, 9, 1310, {'1%': -2.5674488310704504, '5%': -1.9412069851207092, '10%': -1.6166188221188553}, -7409.76536344886)
low p-value of ADF test (1.3357913098839414e-19) shows that we will reject null hypothesis. 
 Hence, the residual is close to stationary.
Data is not getting stationary by multiple differencings. So data is trend stationary.
<img width="483" alt="Screen Shot 2023-01-13 at 1 22 40 AM" src="https://user-images.githubusercontent.com/34772344/212167244-5c02b9b3-ea36-4c17-b29b-91add9055f1d.png">


Results: MLP model
<img width="656" alt="Screen Shot 2023-01-13 at 1 23 59 AM" src="https://user-images.githubusercontent.com/34772344/212167493-65262359-f867-4eb6-b2ce-1b7664dd4595.png">


Results: Vanilla LSTM model
<img width="665" alt="Screen Shot 2023-01-13 at 1 24 29 AM" src="https://user-images.githubusercontent.com/34772344/212167598-be13fa7e-df2b-4178-a4b3-4405ea0a69bc.png">


Results: Stacked LSTM model
<img width="655" alt="Screen Shot 2023-01-13 at 1 24 59 AM" src="https://user-images.githubusercontent.com/34772344/212167678-cee0cc97-3b1d-4f25-a2b1-dd869c7d16f2.png">


Results: Bidirectional LSTM model
<img width="655" alt="Screen Shot 2023-01-13 at 1 25 21 AM" src="https://user-images.githubusercontent.com/34772344/212167748-d8dd2283-8681-4261-99a3-120a8488dbdf.png">


Performance Metrics
<img width="940" alt="Screen Shot 2023-01-13 at 1 27 27 AM" src="https://user-images.githubusercontent.com/34772344/212168198-bc6e221e-2491-4ca8-8ee8-875463e22e6c.png">


