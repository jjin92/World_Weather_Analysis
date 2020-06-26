# World_Weather_Analysis
Module 6
## Challenge
### Part 1: Get weather description and Precipitation
#### Instruction:
- Generate 500+ new cities
- Use OpenWeatherMap API call to gather following data for each city, and export dataframe into csv file
  - Latitude and longitude
  - Maximum temperature
  - Percent humidity
  - Percent cloudiness
  - Wind speed
  - Weather description (e.g., clouds, fog, light rain, clear sky)
  - The amount of rainfall over the last hour (1 hr).
  - The amount of snowfall over the last hour (1 hr)
#### Lessons learned:
- Try-Except block will skip the append() if error happens. Will need to outdent the append() block and move below the try-except
- Use nested conditions for try-except if multiple conditions needs to be checked

### Part 2: Have Customers Narrow Their Travel Searches Based on Temperature and Precipitation
#### Instruction
- Provide 4 prompts for user to narrow down research
- Based on user's preference, use Google Map API to find the nearest hotel for each city
- Export the hotel dataframe to csv
- Plot a google map with city markers. Each markers will contain info box with location and weather data
#### Result
- ![preferred_city_markers](https://github.com/jjin92/World_Weather_Analysis/blob/master/image/WeatherPy_vacation_map.PNG)
#### Lessons learned
- When using df.loc with multiple conditions, make sure to add () between the two & statements
- When gmaps does not display in jupyter, make sure the widgets are enabled. https://stackoverflow.com/questions/45779271/google-map-does-not-display-correctly-in-jupyter-notebook

### Part 3: Create a Travel Itinerary with a Corresponding Map
#### Instruction:
- Pick 4 cities in the list from part 2, and use tuple to get (lat,lng) pair
- Create route layer and market layer using Google Map API call
#### Results:
- ![route_image](https://github.com/jjin92/World_Weather_Analysis/blob/master/image/WeatherPy_travel_map.png)
- ![route_marker](https://github.com/jjin92/World_Weather_Analysis/blob/master/image/WeatherPy_travel_map_markers.png)
#### Lessons Learned:
- To generate a tuple from values in a df, can use tuple(zip(df.column1.values,df.column2.values))
- Waypoints is used as middle-points in addition to start and end points for google routes map

