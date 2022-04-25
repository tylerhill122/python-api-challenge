# python-api-challenge - Tyler Hill 4/25/22 #

## ---------WeatherPy--------- ##

The purpose of this repository is to display our ability to use APIs to gather and plot data using Python/Pandas.
We were tasked with randomly generating >500 coordinates with their corresponding latitudes and longitudes, then to grab the
nearest city to these coordinates, accounting for and removing any duplicates. From there we placed those city names into
OpenWeatherMap's "Current Weather Data" API to grab the following pertinent information: 
latitude and longitude, temperature, humiditiy, cloudiness, and wind speed.

From this information a Pandas DataFrame was created and exported as an external .csv file.
We were tasked with creating four plots for the initial data:
    1.) Temperature vs. Latitude
    2.) Humidity vs. Latitude
    3.) Cloudiness vs. Latitude
    4.) Wind speed vs Latitude
Regression lines and values were also calculated, plotting the regression line.
## --------------------------- ##
I chose to create all plots using a single function 'plot()' to avoid excess repetition. This was a decision that caused many
headaches but would utimately be a worthwhile learning experience. I would like to re-visit this exercise and attempt to further
clean-up the plotting function.
## --------------------------- ##
To expand further, the cities were separated into Northern and Southern Hemispheres to allow for more accurate plotting.
The previously-created plotting function was re-used and modified for these plots. Given more time I would like to create a function to plot all plots without excess repetition.


## ---------VacationPy--------- ##
The purpose of this second exercise was to plot our data using Gmaps, limit our results to desired vacation spots,
and to gather hotel information using Google's Place's API.

The second part of this exercise involved importing the external .csv created in 'WeatherPy'.
A DataFrame was created and then plotted using 'gmaps' to create a map displaying the city locations on a map,
with a heatlayer signifying the relative humidity of each city.

We were then asked to declare our ideal weather conditions when choosing a vacation location.
I chose the following parameters which narrowed down the data to just 9 cities:
    1.) Temperature in range 75 - 82 (degrees F)
    2.) Wind speed in range 0 - 10 (MPH)
    3.) Cloudiness in range 0 - 10 (%)
Google Place's API was used to search each city for the closest hotel, these hotel locations (based on geocoordinates) were
then added to the previous heatmap to display vacation options.