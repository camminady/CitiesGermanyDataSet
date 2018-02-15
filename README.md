# REMARK, ERROR # 
Inside of DISTANCESPHERE, the actual data is the angle (in deg) of the great-circle. To get the distance in km, perform DISTANCESPHERE*/360*2*pi*6371. Also note, that DISTANCECAR is in miles.

# Cities Germany Data Set # 
The repository CitiesGermanyDataSet contains the distance between the 79 largest cities in Germany.
Distance is measured in the following ways
	1) As the great-circle distance between two cities given the radius of the earth as R=6371km
	2) As the shortest distance that Google Maps suggest for a carride between the two cities
	3) As the duration for the trip listed in 2)

## About the data ##
We took the 79 largest cities of Germany from Wikipedia (https://en.wikipedia.org/wiki/List_of_cities_in_Germany_by_population). 
Using the Google Maps API, we calculated the distance for a road trip from one city to all other cities, repeating this process for every of the 79 cities. 
Therefore we obtain a matrix for the duration of a trip from one city to another, as well as for the distance. Additionally, we used the coordinates from the same Wikipedia article and the radius of the earth to compute the great-circle distance between two cities.

## About the Google Maps API procedure ##
As the amount of request via the Google API is limited, all data has been obtained over the course of three days. For cities 1 to 32 data was obtained on the 14th of Feb 2018 at 7pm, for cities 33 to 60 on the 14th of Feb 2018 at 10am and for 61 to 79 on the 15th of Feb 2018 at 11am.

### The problem of traffic jams ###
The duration for a trip might be longer then usual, if there was a traffic jam on that route at that day.

## About the files and folders ##
The folders TXT and MAT contain 5 files each. The files have the same names except for the ending (which is either .txt or .mat). 

