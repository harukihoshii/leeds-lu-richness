# Accessibility to land use in Leeds
## Overview
This repository records a basic use of the pandana package using Leeds as an example. Using datasets solely from OpenStreetMap (OSM), Land Use Richness was calculated to represent how "rich" or varied the area around your building is in terms of different kinds of places you can easily reach within a 10-minute walking distance. This is not meant to indicate how varied the land uses are within that building, which could also be an interesting measure. The final result is shared using MapLibre GL JS, and Maptiler is used for the basemap. You can view it [here](http://harukihoshii.github.io/leeds-lu-richness/). 

## Basic workflow
Using building footprints, Points of Interest (POIs), and walkable networks from OSM via OSMnx and pandana, the pandana function counts all the POIs that can be reached from the junction of the street nearest to the building within a 10-minute walking network distance. The POIs were categorized into 7 land use types. Finally, richness was calculated by assigning a value of 1 if the land use category was accessible within 10 minutes and summing these values. If you can't reach any of the land uses within 10 minutes, your score is 0, meaning the area doesn't have access to any land use.

