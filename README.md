# MUSA611_Final
Final Project for MUSA611 Spring

Leanne Chan  
47188003  
llchan@design.upenn.edu

https://leannechan.github.io/MUSA611_Final/

# Dengue Hot spots Score Builder in Singapore 
Dengue fever is spread by ades mosquitos and has been a problem in Singapore for many years. The main purpose of the application is for planners to idenitfy ares which might be dengue hotspots, allowing them to prioritize ares for mosquitio fogging. This is especially important given the current coronavirus situation where almost half of Singapore's migrant worker workforce has been quarantined, and services like fogging have been affected. 

## The data

CRS used: EPSG:3414 (Singapore)

The application plans to have one map layer showing currently identified dengue clusters: https://data.gov.sg/dataset/dengue-clusters. 

Another layer (accessed via a drop down menu) will show data aggregated by subzones. 
This data includes:
  -  The population density and mean population age in each subzone: https://data.gov.sg/dataset/singapore-residents-by-subzone-age-group-and-sex-june-2016-gender. The current data needs to be divided to achieve the population density and mean age. This will be done in ArcGIS. The shapefile will then need to be converted to a geoJson. (https://idfg.idaho.gov/blog/2014/08/basic-steps-converting-arcmap-shapefile-geojson) 
  
  - The number of dengue clusters in the subzone (will have to be aggregated to the subzones. This can be done in ArcGIS)
  
  - The number of active construction sites (these are potential breeding grounds) in each subzone. https://www.bca.gov.sg/Professionals/IQUAS/IQUAS/QmProjects.aspx. This data needs to be geocoded. Could use Mapbox API to get lat lngs of the addresses listed in the table. 
 
- For layer 2, the idea is to allow the user to select which of the three metrics they would like to see on the map. And if more than one metric is selected, those selected are added together. A choropleth map will show the varying risk of dengue across the subzones. 

## Technologies used

- Leaflet maps 
- Button functionality 
- MapBox API , for geocoding and maybe even routing (if time permits, will add functionality to see distance to nearest hotspot) 
- Slide model: To switch between the dengue cluster layer and the subzone layer. 

Which technologies covered in class (or discovered on your own!) do you
plan to use? How do you anticipate using each of these technologies?

Review the APIs/online examples of leaflet, turf, jQuery, underscore (or
any library not explicitly covered in class) for functions/uses which
you'd like to explore. Briefly describe how you might use them.

## Design spec

#### User experience
The users will be planners who want to identify which areas of Singapore need mosquito fogging ASAP. 

#### Layouts and visual design

There will be a side bar for the user to select which metrics they would like to see in their dengue risk scheme. 
There will be a drop down menu on the top right hand corner allowing the user to switch between the 'slides'. 

## Anticipated difficulties

Aggregating the metrics together when the user clicks on the option.

## Missing pieces

Rather specific to Singapore, but I am interested in using the OneMap API: https://docs.onemap.sg/#introduction

