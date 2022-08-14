# World_Weather_Analysis

## Overview of the Project
---
The purpose of this project is creating an app that can provide Travel recommendations based on weather criteria. Using a database of destionations around the World and asking the user for a set parameter of minimum and maximum desired temperatures during the vacation.

## How does it works?

Using the OpenWeather API as well as Google Maps API's the first step is to generate a set amount of random longitudes and latitudes to use them with CityPy to ping for nearby cities and store them in a Pandas Dataframe after using the Google Maps API to request Hotels for each city and store it in a csv file.

![request_latlong](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Resources/request_latlong.png)

![hotel_df](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Resources/hotel_df.png)

After having the csv file, we then ask the user to define parameters for the desired minimum and maximum temperatures during their trip.

![request_temp](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Resources/request%20usertemp.png)

With those parameters we create a new DataFrame that only contains the cities within those ranges of temperatures and create a figure using Google Maps API for the user to visualize the information.

![hotel_df_map](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

We then ask the user to select 4 desired destinations and using the Google Directions API trace a route itinerary to visit the 4 cities.

After having the itinerary we display both the route and suggested hotels in two maps.

![itinerary_hotels](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)

![travel_map](https://github.com/carloshgalvan95/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)

In this case the parameters for temperature were **Min:** 10 Celsius and **Max:** 15 Celsius. And the suggested itinerary:

| **Country** | **City**    | **Hotel**                             |
|-----------|----------------|--------------------------------------|
| Australia | Codrington     | Codrington Gardens Bed and Breakfast |
| Australia | Mount Gambier  | The Commodore                        |
| Australia | Bendigo        | The Hotel Shamrock                   |
| Australia | Lakes Entrance | The Esplanade Resort & Spa           |




