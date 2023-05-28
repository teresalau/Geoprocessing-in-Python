## Geoprocessing-in-Python
### A geospatial data manipulation project in Python

To understand the impact of the COVID-19 pandemic and its recovery on the traffic to two neighbourhoods in Toronto which are Spadina Chinatown and Liberty Village, I used Python to manipulate geospatial data into shape files to enable further visualizations in QGIS. 

### 1. Data Sources
Two datasets were used in this project - mobile traffic data and the Canadian Historical Business data. The former proprietary dataset was provided by Environics Data, an analytics company and an industry partner of the course MUI2000 led by Professor Karen Chapple and Jeff Allen from the Ubiversity of Toronto. The latter one is part of the collection in the Maps and Data Library at the University of Toronto.

### 2. Geoprocessing in Python
In the mobile traffic data, the number of individuals originating from the same location as recorded by latitude and longitude to each of the neighbourhood were aggregated. However, to visaulize the flow of traffic coming from one spot to another in QGIS, the coordinates data needed to be coverted to shape files. Thus, geoprocessing packages [Geopandas](https://geopandas.org/en/stable/) and [Shapely](https://shapely.readthedocs.io/en/stable/manual.html) were used to transform coordinates into lines that connect the points of origins to the destinations.

As for the Canadian business data, our team sought to understand the type and number of business in each of the Toronto neighbourhoods of interest. The original dataset consisted of business information such as name, address, postal code, industry, and contact info. However, to visualize the business on a map, coordinates are the requirement. Therefore, the [GeoPy](https://geopy.readthedocs.io/en/stable/) package was used to map the address into coordinates so that I can visualize the datapoints as dots on the map. Specfically, the team is interested in looking at restaurants as sector, so I fitered the data based on the [North American Industry Classification Systems](https://www23.statcan.gc.ca/imdb/p3VD.pl?Function=getVD&TVD=1181553&CVD=1181554&CPV=72&CST=01012017&CLV=1&MLV=5) to include only subsector 722 - Food services and drinking places.

### 3. Results
The exciting part comes when the data is being imported and visualized on QGIS! Let's check out the difference in traffic to Spadina Chinatown between 2020 and 2021. 

#### Unique Visits to Spadina Chinatown from across the GTA (2020)

![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/25714a6f-bde1-460e-a8af-95623a23288b)

#### Unique Visits to Spadina Chinatown from across the GTA (2021)
![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/ef620c48-4b4b-4cf9-bd51-a8990fdc50b1)

It goes without saying that the difference was quite substantial between the two year. Traffic in coming from outside the boundary of Toronto was much heavier in 2021 compared to 2020, and the traffic coming from without the city also increased as well. 

As for the type and number of restaurants in the boundary of each of the neightbourhood. I used QGIS to map out a 100m buffer of the neighbourhood and only query data points that intersected with the set boundary. Here's the difference in the location and type of restaurants in each of the neighbourhood.

#### Restaurants within 100m of Liberty Village by Type (2020)
![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/0799a011-d605-47b8-8466-744bdd15a7cd)

#### Restaurants within 100m of Liberty Village by Type (2020)
![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/d7738f75-091d-4276-ac47-8f9b68f42ade)

As observed on both maps, restaurants in Spadina Chinatown were primarily made up of full-service restaurants as denoted by the green dot with only 11% of restuarants were not a full-service one. In Liberty Village, there were a mix of different types of restaurants and over 31% of those were not full-service restaurants. 

### 4. Reach out to me if you want to collaborate! 
I thoroughly enjoyed the process of creating maps and using Python to manipulate data for geospatial analysis. If you have any thoughts or questions about this project, or are looking for people to contribute to your geospatial projects, please do not hestitate to reach out to me via [LinkedIn](https://www.linkedin.com/in/teresacmlau/).
