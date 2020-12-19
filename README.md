# Sightseeing along the route

Building AI course project

## Summary

A web app that finds places of interest between starting point and the destination, and suggests optimal route through them.


## Background

When taking a roadtrip, I know where I'm embarking from and where is the final destination at. The best route between those two points is easy to plot. Instead of just driving non-stop, let's say from Vantaa to Ruka, I'd like to see points of interest along that route, within reasonable deviation from the fastest route. One could search places manually, but it gets harder the longer the route is, especially since attractions are often grouped by city or municipality.

![Route example](https://github.com/Merlac/TSP-sightseeing/blob/main/TSP-sightseeing.jpg?raw=true)


## How is it used?

The user would input the point of departure, the destination and the amount of allowed deviation measured in time or distance. The app would respond with points of interest in map view and an optimal course already plotted through them.

The detours could be filtered (in advance or afterwards) based on interests and needs, such as museums and restaurants. The amount of detours could be suggested automatically, if opening times of attractions, time of departure and total allowed travel time are known.


## Data sources and AI methods
The most important data sources in the app would be [Tripadvisor API](http://developer-tripadvisor.com/content-api/) for places of interest and [Google Directions API](https://developers.google.com/maps/documentation/directions/overview) for routing. For more advanced timing and detailed routing opening hours could be pulled from [Google Places API](https://developers.google.com/places/web-service/details), if not provided by the Tripadvisor API.

Before the final routing through Google Directions API, a rough optimal route between selected places could be calculated using AI methods suitable for solving the Travelling Salesman Problem.

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
