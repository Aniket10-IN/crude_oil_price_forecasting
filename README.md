### crude_oil_price_forecasting
Data Source: data.nasdaq.com

Objective: Nasdaq has provided crude oil prices(Dollar per barrel) from Jan 1986 to Feb 2022. I have tried to implement SARIMA model to forecast prices. Training data is till 2017 and I have used 5 year of data as test dataset. 

The data here does not have fixed frequency, it has total of 9024 records i.e there have been missing days when the price were not given. In order to have a fixed frequency, I have calculated mean of every month and this reduced the shape to (434,1). And my goal is fit a model such that it reduces the error
and somehow able to predict as close as possible. In order to test SARIMA model, I have created a baseline model which directly gives the last 60 months 
of training data as a prediction for  our test data.

Conclusion: Predicting crude oil prices depends a lot on several other factors inspite of past values. Although the SARIMA model doesnot yeilds a good score, it is still way better than the baseline model. I just wanted to implement my learning on real life data to gain better understanding of the topic.

Decomposition 
![decomposition](https://user-images.githubusercontent.com/76424351/232764302-9829352f-fa96-4173-9b03-4ec1d267fca6.png)

Residual Analysis(QQ plot)
![QQ_plot](https://user-images.githubusercontent.com/76424351/232764444-3565ff2f-0b50-4545-a0d5-7012a44ce1bb.png)

Final Mape score
![mape](https://user-images.githubusercontent.com/76424351/232764531-69343ea6-cd66-4fa0-b927-b399124de19d.png)
