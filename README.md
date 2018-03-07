# Prediction on Parking Availability in SF

This repo documents our work for the final project of Advanced Machine Learning course of M.S. in Data Science program at University of San Francisco. 

The goal of the project is to predict whether a parking spot is available at a given date time on a given street for the time period between March 2014 and November 2016. We used all three datasets provided for the model, namely 'train-parking.csv', 'ParkingSensorData.csv', and 'parkingrecords.csv'. We refer them as training data, sensor data, and records data respectively.

For better version control and easier future reference we have put our work to four separate folders as shown above. Below we describe the contents in each folder.

### Data Folder:
#### This foler keeps aggregated/processed data files so we can later directly join them with other datasets.
- aggregated_sensor.csv: aggregated sensor data (calculated spots & occupancy percentage)
- pr_streetmatch.csv: parking record meter data matched to each individual street pairs
- sensor_longlat.csv: the geo encoding of unique block address in sensor data
- train_longlat.csv/train_longlat_full.csv: the geo encoding of unique Streets, From_To pairs in training data 
- validation_set.csv: validation set

### Features Folder:
#### This folder documents our efforts in generating different features for the model.
- EDA: EDA on the training data and visualization of the coordinates in the three datasets
- EDA_validation_set/EDA_validation_set_updated: Generate a reliable validation set using the test data distribution
- geocode_sensor: Get the longitude and latitude of the street blocks in the sensor data
- parking_record_match: Map the meter coordinates in the records data to the streets in the training data, and perform aggregation by street and time-related features
- process_parkingrecords: Convert the time string in the records data to time-related features
- long_lat_table_217:  Get the longitude and latitude of the streets in the sensor data
- sensordata: Calculate the average occupancy rate for different time types by street in sensor data

### Models Folder:
#### This folder contains all the models that we have tuned and run.
The final_model.ipynb is the one we used to generate our final Kaggle submission output. The subfolder, Old_Models,  has all other models for which the filenames indicate the date that we ran the model and made a submission. 

### Submission Folder:
#### This folder includes a subset of our submissions that we deem useful to keep track of.
