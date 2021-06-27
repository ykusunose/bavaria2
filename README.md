# bavaria_wheat_trials_2
Winter wheat trials in Bavaria, Germany (2000-2019): Sites and varieties grown.
## This map
This map shows the locations of variety trial sites (places where they grow new crop varieties to assess their performance) for winter wheat in Bavaria, Germany from 2000 to 2019. The number of varieties tested varies by site, and also by year. To deal with this, I incorporate a year slider so that the user can specify the year. The number of varieties at each site (in that year) is represented by the size of the circles representing each site. 

Suppose the user wishes to know how many varieties were tested in a location called Reith, in the year 2000. Not only would they see the number (17), but also the names of those 17 winter wheat varieties.

## The data depicted
1. the number and names of varieties at each site, each year (these are publicly available at https://www.lfl.bayern.de/ipz/getreide/019108/index.php, but my colleague put these all together into a usable file).
2. agro-ecological zones 2013, Julius Kühn-Institut (the shapefile came via the German Statistics Office for Land and Agriculture).
3. current wheat-growing regions, Data: Stat. Ämter der Länder, Kreisdaten der Landwirtschaftszählung 2016 (eigene Berechnungen);
                    FDZ der Stat. Ämter des Bundes und der Länder, Landwirtschaftszählung 2010 and AFiD-Panel
                    Agrarstruktur 1999, 2003, 2007, 2016 (eigene Calculation: 1999-2016. Clusterschätzer);
                    © GeoBasis-DE/BKG (2016) (this shapefile also came from the German Statistics Office for Land and Agriculture).

## The tools used
1. geojson.io to places the addresses of the trial sites onto a map.
2. Mapshaper to convert geoJSON files of basemap polygons to topoJSON files--which are more parsimonious.
3. QGIS to select only the polygons that cover Bavaria (also to reduce file sizes).
4. QMetaTiles, a QGIS plug-in, to convert the basemap polygons into tilesets.
5. Leaflet for mapping and map UI.
6. Mapbox API for the formatting of the page (I think).
