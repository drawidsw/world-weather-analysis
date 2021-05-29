# world-weather-analysis

## Deliverable One:

First, 2000 random latitudes and longitudes were generated and the **citipy** module was used to find nearest cities to each coordinate. A total of 761 unique cities were found.

Next, the openweatherAPI was used to find weather information of each city. OpenweatherAPI was able to find 701 (of the 761 requested) cities and returned responses for those. The relevant weather data was retrieved from each response and through a pandas dataframe, it was dumped to a CSV file eventually. The CSV file link is here:
[a relative link](WeatherPy_Database.csv)
