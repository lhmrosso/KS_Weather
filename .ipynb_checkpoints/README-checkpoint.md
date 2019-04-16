# KS_Mesonet
*Getting weather data with python 3*  

<br>

**Author**: Luiz Moro Rosso  
**Semester**: Spring 2019  
**Project area**: Agronomy  
**Kansas State University**

## Objective
Retrieving weather data from the crop growing season for Lat/Long coordinates in the state of Kansas.

## Outcomes
One .csv file with all the [weather variables](http://mesonet.k-state.edu/rest/variables/) for specific Lat/Long coordinates and time intervals (from planting to harvest). from the closest Mesonet station to a Lat/Long coordinate.

## Rationale
Exploring weather variables is primordial to understand plant-soil interactions and crop response to management practices, but data acquisition is time-consuming, and the output is pretty variable depending on the available sources. Also, weather stations occasionally experience issues with sensors and data recording, complicating further analysis.

National Centers for Environmental Information (NCDC) has a [webpage](https://www.ncdc.noaa.gov/) for providing land stations weather data across the entire US. However, even with a relatively easy interface, a python script to **download** ([link](https://www.ncdc.noaa.gov/cdo-web/api/v2/data?datasetid=GHCNDMS&locationid=ZIP:28801&startdate=2000-01-01&enddate=2010-01-01)), **clean**, and **organize** datasets would be helpful in research projects with many experimental locations or exploring many weather variables.

As the first step, the python code needs to get the user input (Table 1), identifying which is the closest weather station based on the Lat/Long coordinate. The variables will be downloaded in a *daily bases* from the start to the end date (period of interest). As soon as the data is imported, a function to replace values will be build for each variable. For temperature, for example, the empty rows will be replaced with the average of the previous and next day.

**Table 1.** Example of user inputs.

| Start date     |    End date    | Latitude       |   Longitude    |
|:---------------|:---------------|:---------------|:---------------|
| 01/01/2018     |  01/01/2019    |  39.4948585    | -96.494858     |

## Sketch

<img style="float: left;" src="sketch.jpeg" alt="sketch_image" width="700"/>

## References
Young, A. H., K. R. Knapp, A. Inamdar, W. B. Rossow, and W. Hankins, 2017: “The International Satellite Cloud Climatology Project, H-Series Climate Data Record Product”, Earth System Science Data, in preparation.
