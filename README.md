# Case_Study_1-Annual_Bike_Membership_Increase
Case Study 1: How does a bike-share navigate speedy success?

The analysis is related to a case study presented by the Google Data Analytics through Coursera. 

The data has been processed and analyzed in R but could be done through spreadhsheets or SQL as well.

Sources Used: 
Divvy 2019 Q1 dataset by Motivate International Inc. under their license (https://divvybikes.com/data-license-agreement).
Divvy 2020 Q1 dataset by Motivate International Inc. under their license (https://divvybikes.com/data-license-agreement).
Note: To protect sensitive information, data does not provide information to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes in the time periods provided.

Assumptions made for this analysis:
- The data is from an outside source. It is assumed the data source is credible and reputable.
- The column names are different in 2019 and 2020 datasets. It is assumed there are some columns that are collecting the same information despite these column names such as (started_at (2020) and start_time (2019), ended_at (2020) and end_time (2019), start_station_name (2020) and from_station_name (2019), end_station_name (2020) and to_station_name (2019), start_station_id (2020) and from_station_id (2019), end_station_id (2020) and to_station_id (2019), member_casual (2020) and usertype (2019).
- One record has been removed from this analysis because had null values for end station name and id and a negative trip duration. It is assumed this was either an error data point or test data point.
- It is assumed Subscribers in usertype (2019) is the same as members in member_casual (2020) and Customers in usertype (2019) is the same as casual in member_casual (2020).
- For the purpose of this analysis, if a record has the same start time, end time, start station and end station as another record, it will not be removed from the analysis unless there’s a shared ride ID as they could be individual riders that started and ended at the same time and destination.
- For this analysis records with ride length of less that 24 hours will be used as in most cases a person cannot stay up passed 24 hours. 482 records were found above 24 hours, these are all considered outliers, not in scope to the business task and will not be used in this analysis.
