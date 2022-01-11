# MINKT Stories Web Map

The MINKT Stories web map is an open layers web application that integrates data collected in Survey123 as a WFS. The application includes pop-ups, geolocation, an interactive gallery, and layer switchers ([walkermatt-layerswitcher](https://github.com/walkermatt/ol-layerswitcher)).

**See the Web Map Result:** <br/>
[https://zgis.github.io/minktstories_webmap/](https://zgis.github.io/minktstories_webmap/)

**View the MINKT Stories Platform:** <br/>
[https://minkt-stories-lungau.zgis.at/](https://minkt-stories-lungau.zgis.at/)


<br/>

![image](https://user-images.githubusercontent.com/81073205/143590945-9ffa7b3e-0f4c-4597-8e14-29defc484a87.png)

<br/>
<br/>

**Recent Updates:** 
<br/>

| _Date_  | Issue / Edit |
| ------------- | ------------- |
| _11.01.2022_  | Token had to be updated (again). |
| _05.01.2022_  | Token had to be updated (again). |
| _04.01.2022_  | Token had to be updated (again). |
| _21.12.2021_  | **ol.proj.transform()**: The features from the WFS no longer showed up on the map today. Upon investigation it turns out the coordinates of each point was being coverted completely wrong (some points had invalid coordinates, some were in Canada, and some were in Antarctica). Only after removing the ol.proj.transform function from the point geometries wsa the issue resolved and the points again appear in their correct location. Oddly, the geolocation and the home position still function properly with the transformation function. Note: no changes were made to the survey, the WFS, or the source code of this web map when I noticed the missing features.  | 
| _14.12.2021_  | Survey123 **token** updated again. While working on another project in ArcGIS Online the user was logged out. This triggered a safety issue and an caused an automatic update for the tokens. It is the same issue as experienced before (30.11.2021). |
| _07.12.2021_  | Legned updated with improved icons and css styling. |
| _01.12.2021_  | Legend added. Some stylistic improvements. |
| _30.11.2021_  | The survey123 **tokens** (used for image URL generation) were changed by ESRI. It is unclear whether this automatically happens every 2 weeks or if the token change was triggered through activity in ArcGIS Online (at the time when the tokens were changed, a user was editing the MINKT platform, not the web map, and an error message was issued regarding the tokens). to fix the issue, the tokens were updated in the code.  |
|  _30.11.2021_  | Added to the map: autoPan function for the pop-ups, on-hover highlighting of the individual features, and an on-hover opening and closing of the layer switcher menu were added.  |

<br/>
<br/>

**Contributors:** <br/>
Niklas Jaggy, Katharina Wöhs, Christina Zorenböhmer

**Current Bug Log:** <br/>

| _Issue_  | Date | Details |
| ------------- | ------------- | ------------- |
| _autoPan_  | 01.12.2021 | When clicking on a feature, the autoPan sometimes only works on the second click. There is an issue of duplicate code for the feature pop-ups (one version needed for the gallery that does not include autoPan, and one for the features in the map, which does include autoPan. |
|  _Feature Clustering_  | 01.12.2021 | Feature clustering layer currently does not take into account which feature categories are turned on and off in the layer switcher.  |

<br/>

**Create a New MINKT Story yourself:** <br/>
Go to [Survey123](https://survey123.arcgis.com/share/b6e023860648421f832ce0e93ad14aec) and simply upload a new story. <br/>
<img align="center" src="https://user-images.githubusercontent.com/81073205/144023964-5ae8c0b1-2d0c-480d-9278-e644319403a5.png" width="200" height="200">
