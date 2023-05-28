## Geoprocessing-in-Python
### A geospatial data manipulation project in Python

To understand the impact of the COVID-19 pandemic and its recovery on the traffic to two neighbourhoods in Toronto which are Spadina Chinatown and Liberty Village, I used Python to manipulate geospatial data into shape files to enable further visualizations in QGIS. 

### 1. Data Sources
Two datasets were used in this project - mobile traffic data and the Canadian Historical Business data. The former proprietary dataset was provided by Environics Data, an analytics company and an industry partner of the course MUI2000 led by Professor Karen Chapple and Jeff Allen from the Ubiversity of Toronto. The latter one is part of the collection in the Maps and Data Library at the University of Toronto.

### 2. Geoprocessing
In the mobile traffic data, the number of individuals originating from the same location as recorded by latitude and longitude to each of the neighbourhood were aggregated. However, to visaulize the flow of traffic coming from one spot to another in QGIS, the coordinates data needed to be coverted to shape files. Thus, geoprocessing packages [Geopandas](https://geopandas.org/en/stable/) and [Shapely](https://shapely.readthedocs.io/en/stable/manual.html) were used to transform coordinates into lines that connect the points of origins to the destinations.
