# ANA-515-Assignment-3

## **Overview**
The data is obtained from NOAA’s Storm Events Database. This data lists major weather-related storm events since 1950. For each event, it includes information like the start and end dates, where it happened, associated deaths, injuries, and property damage, and some other characteristics. Each row is a separate event. However, often several events are grouped together within the same episode. Some of the event types are listed by their county ID (FIPS code) (“C”), but some are listed by a forecast zone ID (“Z”). Which ID is used is given in the column CZ_TYPE. 

## **Data Wrangling and Cleaning steps:**

1.	Data downloaded from https://www1.ncdc.noaa.gov/pub/data/swdi/stormevents/csvfiles/ for the year 2013. Data movied into the current working directory and read and saved. (5 points)
2.	The dataframe is restricted to the following columns: (10 points)
•	BEGIN_YEARMONTH
•	EPISODE_ID
•	STATE
•	STATE_ FIPS
•	CZ_NAME (this is the county name)
•	CZ_TYPE
•	CZ_FIPS
•	EVENT_TYPE

3.	The data arranged by the state name (STATE) (5 points) 

4.	State and county names changed to title case (e.g., “New Jersey” instead of “NEW JERSEY”) (5 points) 

5.	 Data limited to the events listed by county FIPS (CZ_TYPE of “C”) and the CZ_TYPE column is removed(5 points) 

6.	The State and County FIPS are padded with a “0” at the beginning (hint: there’s a function in stringr to do this) and then unite the two columns to make one FIPS column with the new state-county FIPS code (5 points) 

7.	All the column names are changed to lower case  (5 points) 

8.	There is data that comes with base R on U.S. states (data("state")).It is used to create a dataframe with these three columns: state name, area, and region (5 points)

9.	A dataframe with the number of events per state is created. The state information dataframe that is just created in step 8 is merged with the storm events dataframe. Any state that are not in the state information dataframe are removed. (5 points) 

10.	A plot of the number of events (y) to land area (x) is created. (10 points): 
  




