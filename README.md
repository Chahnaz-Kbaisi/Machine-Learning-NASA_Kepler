# Machine-Learning-NASA_Kepler
![NASA](https://github.com/Chahnaz-Kbaisi/Machine-Learning-NASA_Kepler/blob/main/Images/exoplanets.jpg)

****

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created machine learning models capable of classifying candidate exoplanets from the raw dataset.

The following were used to develop machine learning models: 

# Model 1: Testing Support Vector Classification (SVM)

SVM is a supervised machine learning algorithm that analyze data for the purposes of classification into distinct categories and regression analysis.

To perform the SVM testing model the following steps were taken:
* I read the dataset into  pandas dataframe and dropped any null values
* Then, I examined the dataframe `dtype` and investigated the significance of the columns. `koi_tce_plnt_num` was dropped from the dataframe.
* I created the train test split using `koi_disposition` as the y-value
* Then, the dataframe was scaled using the MinMaxScaler.
* In the SVM training model I followed three steps:
    1. Creating a SVM linear classifier
    2. Fitting the data
    3. Predicting the model
    