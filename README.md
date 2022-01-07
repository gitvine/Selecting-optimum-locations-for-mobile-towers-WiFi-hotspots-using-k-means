# Selecting optimum locations for mobile towers/ WiFi hotspots using k-means
Network planning is an important task in any telecommunication company. We need to provide good coverage at all the required locations at minimum cost. As the number of towers increase, the cost of installation and maintenance also rises. So, we need to install towers in such a way that our target of coverage is achieved with minimum number of towers. In this project, I have tried to achieve this by using data science tools.

## Interest

This kind of implementation of data science can be of interest to telecommunication companies who wish to plan their future networks. Although, I have taken the example of mobile towers in this project but the strategy can be used to plan WiFi hotspots and other radio networks too.

## Data description

### Data sources

I have used Foursquare API to get the list of venues in the target area. We need to provide coverage at all the venues in this list. We need latitude, longitude, venue name from Foursquare around our target location. We selected a target area on map and got its latitude and longitude from google maps. We fetched all the venues in an area of approximately 7X7 Kms centred at our target location.

I am using a free service of Foursquare which gives me a limited number of venues around a location at a time. So, to overcome this I created a square grid (5X5) of 25 locations ( I called them city points ) centred at the target location and then fetched the list of venues for all these locations within their 1 Km radius from Foursquare.
