# Predicting Volcanic Eruptions

*What if scientists could anticipate and predict volcanic eruptions as simple as predicting weather? This would be a huge impact on people living near volcanoes and can potentially save millions of lives all over the world. If scientists could accurately predict a volcano's next eruption, people can evacuate much faster and more prepared, thus limiting damage.

## Data

*Dataset will be coming from kaggle. Although eruptions are hard to detect, scientists do their best by measuring "time to eruption" by analyzing and surveying volcanic temors from seismic signals. In active volcanoes, scientists are able to predict eruptions in minutes in advance but fail at long term predictions. 

Detecting volcanic eruptions before they happen is an important problem that has historically proven to be a very difficult. This competition provides you with readings from several seismic sensors around a volcano and challenges you to estimate how long it will be until the next eruption. The data represent a classic signal processing setup that has resisted traditional methods.

> * [Kaggle Dataset](https://www.kaggle.com/c/predict-volcanic-eruptions-ingv-oe/data)

## Data Wrangling

*Data consists of two fields: segment_id and time_to_eruption. And the training and test set contains ten minutes of logs from ten difference sensors surrounding the volcano. First step is to remove all null values and make segment data into one dataframe. This includes computing the mean, std, min, max, and quantile data per sensor. These will be our features. Next I will be using MinMaxScaler and StandadScalar to normalize data

## EDA

*First I plotted the time to eruption distribution. I seperated the min and max values of time to eruption to analyze each sensor data. Next steps are to filter each different columns into a set and compare these features with a heatmap and scatterplot to spot any correlations among the features. For example, time to eruption vs all 80 different sensor readings. I then created scatterplots, boxplots, and picked a few segment ids to analyze individually to see if other features can be created.


## Modeling/Predictions

*I used 5 different training models as shown in the notebooks (LinearRegression, RandomForestRegressor, LGB, GradientBoostingRegressor, DecisionTreeRegressor) and then applied GridSearchCV parameter to tune each model. At the end, I chose the LGB model because it gave us the best cross validation score. I suspect that if more features were used and created, the score would be lower. 







