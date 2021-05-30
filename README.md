# world-weather-analysis

## Deliverable One:

First, 2000 random latitudes and longitudes were generated and the **citipy** module was used to find nearest cities to each coordinate. A total of 761 unique cities were found.

Next, the openweatherAPI was used to find weather information of each city. OpenweatherAPI was able to find 701 (of the 761 requested) cities and returned responses for those. The relevant weather data was retrieved from each response and through a pandas dataframe, it was dumped to a CSV file eventually. The data is accessible 
[here](Weather_Database/WeatherPy_Database.csv).

## Deliverable Two:

From the 701 cities stored in the first deliverable, the data set was filtered by putting minimum temperature of 30 F and maximum temperature of 80 F. This yielded 488 distinct cities. Then, an attempt to filter rows with empty/null values was made. Here, country codes corresponding to 4 cities were found to be NULL. Although these cities look legitimate, these values were still omitted from the dataset leaving 484 values behind. 

Next, using the Google APIs, the nearest hotel within 5,000 meters was located. Out of 484, only 441 valid hotels were found; the remaining rows were filtered out. The final output with cities, the corresponding hotels and the weather information is [here](Vacation_Search/WeatherPy_vacation.csv).

Finally, using the Google maps API, a heat map of all locations was generated, along with a tooltip displaying relevant information for each location. This heat map is displayed below.

![image_name](Vacation_Search/WeatherPy_vacation_map.png)

## Deliverable Three:

Four cities in Russia are chosen and the using the Google map's API, a **direction layer** is added to show the optimal **driving** path taken to visit all four cities. The image is displayed below:

![image_name](Vacation_Itinerary/WeatherPy_travel_map.png)

Finally, a new figure is created and a **marker layer** with relevant information about the travel destinations on the tooptips appears. The image is displayed below.

![image_name](Vacation_Itinerary/WeatherPy_travel_map_markers.png)

# Further Work

We did not explore how to **overlay** both the direction and marking layers on one another. When the two layers were added to the same figure, one of them didn't show up.
