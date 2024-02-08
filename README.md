# Transform-Load-ETL-process
Create an automated Extract, Transform, Load (ETL) process to extract daily weather forecasts and observed weather data and load it into a live report to be used for further analysis by the analytics team.

## My task

Tasked with creating an automated Extract, Transform, Load (ETL) process, I'm focusing on gathering daily weather forecasts and observing weather data for Casablanca, Morocco. This information will be loaded into a live report to monitor the historical accuracy of temperature forecasts from a single source and station. Initially, I'll target one station and source, extracting actual and forecasted temperatures for noon each day. This proof-of-concept will pave the way for expanding the report to include multiple locations, forecasting sources, update frequencies, and additional weather metrics like wind speed, precipitation, and visibility, supporting broader prediction modeling efforts.

## Data source
For this practice project, I'll use the weather data package provided by the open-source project [wtt.in](wttr.in), a web service that provides weather forecast information in a simple and text-based format. 


## Learning Objectives:
- Download raw weather data
- Extract data of interest from the raw data
- Transform the data as required
- Load the data into a log file using a tabular format
- Schedule the entire process to run automatically at a set time daily

  ## Overview
  ### Weather reporting tasks
Must extract and store the following data every day at noon, local time, for Casablanca, Morocco:

- The actual temperature (in degrees Celsius)
- The forecasted temperature (in degrees Celsius) for the following day at noon

### Code 

Syntax Highlighting 

``` sh
header=$(echo -e "year\tmonth\tday\tobs_temp\tfc_temp")
echo $header>rx_poc.log
// Create a text file called rx_poc.sh
touch rx_poc.sh
// Include the Bash shebang on the first line of rx_poc.sh :
#! /bin/bash
// Make script executable by running the following in the terminal:
chmod u+x rx_poc.sh
// 2.2. Assign the city name to Casablanca for accessing the weather report:
city=Casablanca
// 2.3 Obtain the weather information for Casablanca:
curl -s wttr.in/$city?T --output weather_report


```
   
   


