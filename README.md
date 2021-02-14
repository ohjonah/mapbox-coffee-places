# mapbox-coffee-places

This app implements a simple map with markers and the Places plugin with a search dialogue box. This app should also show the user's location if permissions are granted.
- The markers are located in San Francisco, CA and they represent coffee shops in proximity to MapBox HQ: Blue Bottle and Equator Coffee.
- The saved places are markers of my favorite coffee shops in Seattle: La Marzocco, Olympia Coffee Roasters, and Seattle's Starbucks Reserve.


This app has been tested on a physical device: the Pixel 3.

To run this app, you will have to create an access token and a secret key with the `Downloads:Read` scope.

The access token can be populated in `res/values/strings.xml`. The secret key can be populated in your gradle directory, under `grader.properties`.