# Capstone Project for IBM Data Science Professional Certificate
## Introduction:
#### This project was for the Capstone project for the [IBM Data Science Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-science) hosted by Coursera.
#### The aim of the project was to use machine learning algorithms (k means clustering) to cluster or group data.
#### Original requirement was to cluster geographical areas of a country or city (such as neighborhoods or districts), but in this case the Hong Kong MTR network was experimented with instead.
## Methods:
- Geojson files were exported from [Overpass Turbo](https://overpass-turbo.eu/) to get routes and stations.
- The data was cleaned up and the coordinates were extracted from the GeoJson files. Output shown below:
![MTR network](https://github.com/prtlobo/Coursera_Capstone/blob/71d761c69841890073e9036d6b2497df321f32b2/MTR%20Routes%20and%20Stations.png)
- The Foursquare API was used to collect the top 10 *types* of venues around a 500m radius around each station.
## Results:
- Two K means clustering algorithms were created- One based on the best silhouette score as shown below:
![MTR Cluster K best](https://github.com/prtlobo/Coursera_Capstone/blob/71d761c69841890073e9036d6b2497df321f32b2/MTR%20Cluster%20(kbest).png)
And the other based on the same number of MTR lines (11): 
![MTR K Lines](https://github.com/prtlobo/Coursera_Capstone/blob/71d761c69841890073e9036d6b2497df321f32b2/MTR%20Cluster%20(k%20MTR%20lines).png)
## Findings:
One can see which stations are most similiar to one another in terms of venue types
## Future Work:
Further work can be done to include other data sources, 
such as HK GOV demographical information, using the Google Map API instead,
and tweaking the search radius to bring balance between reducing overlap and maximizing search area (this might develop bias in the algorithm)
