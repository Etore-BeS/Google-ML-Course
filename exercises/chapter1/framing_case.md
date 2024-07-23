# Business Case: Telecommunications Company

## Problem Case

A telecommunications company is facing challenges with network congestion during peak hours, leading to customer dissatisfaction and increased churn rates. They want to predict which areas and times are most likely to experience high network traffic so that they can proactively manage network resources and avoid congestion.

## Framing

### Business Use Case

**Predict areas and times of High Network Traffic** to reduce congestion. Then it could lead to **decrease the churn rates** due to costumer dissatisfaction. Business Benefits could be improved costumer experience and potential cost savings.

### Impact

By identifying areas and times of congestion, the company could destinated resources to it. To satisfact customer and reduce the churn rates. Improved Network Performance, Customer Retention and Potential Increase in revenue from satisfied customer are specific impacts of the model's implementation. 

### Sucess Criteria

The model should correctly predict 90% of all high traffic events and areas and the rate of error must lesser than 10% of false negatives

### Stakeholders

- **Traffic Engineers**: Need the output date to solve the problem on the areas needed.
- **Executives**: Need the problem solved to present better churn rates to the board.
- **Data Scientists**: Need the data and the algorithm to train, test, eval, deploy and monitor the model.
- **Customer Servide**: Need the better experience for the customer to decrease the churn rate.

### Data

Historical data (**Timeseries**) with the Y being the traffic and Xs being latitude, longitude, days, hours and minutes of each traffic data point.

### ML Approach

Forecasting Approach (**Supervised Learning**) The problem is to predict the traffic which is a continuous variable. Than it could be determined a predict traffic threshold to traffic engineers be alerted to act upon it. The forecasting algorithm used could an ARIMA, LSTM if the prior doesn't work well.

### Metrics

- **RMSLE**: Used to check the error squared but focus on penalizing under prediction. So the model would not miss a traffic cogestion.
- **Pearson Correlation**: To check if the predictions are on the same trend of the real data.
- **MSE**: To get a comprehensive evaluation of the error from the model.
