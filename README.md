## Geoprocessing-in-Python
### A geospatial data manipulation project in Python

To understand the impact of the COVID-19 pandemic and its recovery on the traffic to two neighbourhoods in Toronto which are Spadina Chinatown and Liberty Village, I used Python to manipulate geospatial data into shape files to enable further visualizations in QGIS. 

### 1. Data Sources
Two datasets were used in this project - mobile traffic data and the Canadian Historical Business data. The former proprietary dataset was provided by Environics Data, an analytics company and an industry partner of the course MUI2000 led by Professor Karen Chapple and Jeff Allen from the Ubiversity of Toronto. The latter one is part of the collection in the Maps and Data Library at the University of Toronto.

### 2. Geoprocessing in Python
In the mobile traffic data, the number of individuals originating from the same location as recorded by latitude and longitude to each of the neighbourhood were aggregated. However, to visaulize the flow of traffic coming from one spot to another in QGIS, the coordinates data needed to be coverted to shape files. Thus, geoprocessing packages [Geopandas](https://geopandas.org/en/stable/) and [Shapely](https://shapely.readthedocs.io/en/stable/manual.html) were used to transform coordinates into lines that connect the points of origins to the destinations.

As for the Canadian business data, our team sought to understand the type and number of business in each of the Toronto neighbourhoods of interest. The original dataset consisted of business information such as name, address, postal code, industry, and contact info. However, to visualize the business on a map, coordinates are the requirement. Therefore, the [GeoPy](https://geopy.readthedocs.io/en/stable/) package was used to map the address into coordinates so that I can visualize the datapoints as dots on the map. Specfically, the team is interested in looking at restaurants as sector, so I fitered the data based on the North American Industry Classification Systems to include only sub

### 3. Results
The exciting part comes when the data is being imported and visualized on QGIS! Let's check out the difference in traffic to Spadina Chinatown between 2020 and 2021. 

#### Unique Visits to Spadina Chinatown from across the GTA (2020)

![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/25714a6f-bde1-460e-a8af-95623a23288b)

#### Unique Visits to Spadina Chinatown from across the GTA (2021)
![image](https://github.com/teresalau/Geoprocessing-in-Python/assets/113483358/ef620c48-4b4b-4cf9-bd51-a8990fdc50b1)

It goes without saying that the difference was quite substantial between the two year. Traffic in coming from outside the boundary of Toronto was much heavier in 2021 compared to 2020, and the traffic coming from without the city also increased as well. 

As for the type and number of restaurants 
