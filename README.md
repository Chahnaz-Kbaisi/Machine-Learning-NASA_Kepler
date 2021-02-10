# Machine-Learning-NASA_Kepler
![NASA](https://github.com/Chahnaz-Kbaisi/Machine-Learning-NASA_Kepler/blob/main/Images/exoplanets.jpg)

****

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created machine learning models capable of classifying candidate exoplanets from the raw dataset.

The following were used to develop machine learning models: 

## Model 1: Testing Support Vector Classification (SVM)

SVM is a supervised machine learning algorithm that analyze data for the purposes of classification into distinct categories and regression analysis.

To perform the SVM testing model the following steps were taken:
* I read the dataset into pandas dataframe and dropped any null values
* Then, I examined the dataframe `dtype` and investigated the significance of the columns. `koi_tce_plnt_num` was dropped from the dataframe.
* I created the train test split using `koi_disposition` as the y-value
* Then, the dataframe was scaled using the MinMaxScaler.
* In the SVM training model I followed three steps:
    1. Creating a SVM linear classifier
    2. Fitting the data
    3. Predicting the model
* To create a stronger model, the data was scaled and normalized, and adjusted to the unit variance. This reduced the dispersion of the data points for the model. Using Standardscaler to scale the data gave the following scores: 

         Training data score: 0.8916650772458516
         Testing Data Score: 0.8947368421052632
        
* GridSearchCV was used to to run hyperparameters and fit the model to the training set. Changing the parameters did not result in a better score: 0.8888044957393081

Model Rank

![SVM](https://github.com/Chahnaz-Kbaisi/Machine-Learning-NASA_Kepler/blob/main/Images/SVM.png)

## Model 2: Logistic Regression

Logistic regression is a machine learning algorithm that uses datasets to predict a discrete set of outcomes or categories. 

The following steps were taken to perform the logistic regression testing model:
* I read the dataset into pandas dataframe and performed basic data cleaning by dropping any null values.
* I created a train and test split using `koi_disposition` as the y-value
* Then, I scaled the data using `StandardScaler`
* The logistic regression yielded the following training and testing scores: 

         Training Data Score: 0.887659736791913 
         Testing Data Score: 0.8895881006864989 
        
* I applied the GridSearchCV to fit the model parameters, however, it did not improve the scores: 0.6631697581848216

Model Rank 

![Logistic Regression](https://github.com/Chahnaz-Kbaisi/Machine-Learning-NASA_Kepler/blob/main/Images/Logistic_Regression.png)

### Summary: 
Both the models appeared to provide similar training and testing data scores. Moreover, tuning the hyperparameters didn't have any affect on the models. In conclusion, the SVM model yielded marginally better scores than the Logistic Regression.   
