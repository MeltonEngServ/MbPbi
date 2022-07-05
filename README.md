# MbPbi: Library to update MapBox with MSSQL Data

**Version 0.2.0**

This is a code that facilitates the creation of Mapbox tilesets using Mapbox Tileset
Service API.


## Installation

Since this library relies in geopandas to handle the geopgraphic data from MSSQL it is important to follow the next steps to set up all the dependancies without problem.

**1. Setting the environment**
    * If not already create a folder of Virtual Environments using UI or powershell.
    ```
    PS C:\Users\username> mkdir VirtualEnvs
    ```
    * Using powershell or the Command Prompt navigate to that folder.
    ```
    PS C:\Users\username> cd "\path\to\VirtualEnvs"
    ``` 
    * Create Python virtual environment inside that folder.
    ```
    PS C:\Users\username\VirtualEnvs> python -m venv geo-env 
    ```
**2. Setting the envrionment**    
    


In order to use this Library you will need to download all the dependencies, most of them would be downloaded as part of this library. However shapely, fiona, pyproj and rtree might need to be installed manually using the windows wheels.

1. [Pandas](https://pandas.pydata.org/getting_started.html)
2. [Geopandas](https://geopandas.org/en/stable/getting_started/install.html)
3. [Pyproj](https://pyproj4.github.io/pyproj/stable/installation.html)
4. [Shapely](https://www.lfd.uci.edu/~gohlke/pythonlibs/#shapely),
[fiona](https://www.lfd.uci.edu/~gohlke/pythonlibs/#fiona),
[rtree](https://www.lfd.uci.edu/~gohlke/pythonlibs/#rtree) 
5. [pymssql](https://pypi.org/project/pymssql/)
6. [geojson](https://pypi.org/project/geojson/)
7. [jsonschema](https://pypi.org/project/jsonschema/)


## Contributors
- Cristian Jara Infante <cristianj@melton.vic.gov.au>

## Functionalities
The current version supports the following data sources:

1. Microsoft SQL Server geometry databases.
2. GeoJson data from a URL.
3. Shapefiles from local directories.

This version also supports the data transformation function clip using 2 layers,
where at least 1 must be polygon.

Since Mapbox does not allow complex geometries like MultiPolygon, MultiLinestring or 
Geometry Collection, this package will try to convert these geometries to simple ones
and this might result in some topology loses.


## Licence
