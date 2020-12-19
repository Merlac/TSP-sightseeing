# Sightseeing along the route

Building AI course project

## Summary

A web app that finds places of interest between starting point and the destination, and suggests optimal route through them.


## Background

When taking a roadtrip, I know where I'm embarking from and where is the final destination at. The best route between those two points is easy to plot using Google Maps, for example. Instead of just driving non-stop, let's say from Vantaa to Ruka, I'd like to see points of interest along that route, within reasonable deviation from the fastest route. One could search places manually, but it gets harder the longer the route is, especially since attractions are often grouped by city or municipality.

![Route example](https://github.com/Merlac/TSP-sightseeing/blob/main/TSP-sightseeing.jpg?raw=true)


## How is it used?

The user would input the point of departure, the destination and the amount of allowed deviation measured in time or distance. The app would respond with points of interest in map view and an optimal course already plotted through them.

The detours could be filtered (in advance or afterwards) based on interests and needs, such as museums and restaurants. The amount of detours could be suggested automatically, if opening times of attractions, time usually spent at the locations, time of departure and total allowed travel time are known (they are, thanks Google!)


## Data sources and AI methods
The most important data sources in the app would be [Tripadvisor API](http://developer-tripadvisor.com/content-api/) for places of interest and [Google Directions API](https://developers.google.com/maps/documentation/directions/overview) for routing. For more advanced timing and detailed routing opening hours could be pulled from [Google Places API](https://developers.google.com/places/web-service/details), if not provided by the Tripadvisor API.

Before the final routing through Google Directions API, a rough optimal route between selected places could be calculated using AI methods suitable for solving the Travelling Salesman Problem.

## Challenges

The plan sounds simple enough and in theory the data should already be available, but it's hard to estimate how precise or resouce hungry the attraction finding would be. For a pleasant user experience the suggestion(s) should be calculated as fast as a Google Maps route query, or at least as fast as the plane ticket finder at Supersaver.

## What next?

A proof-of-concept could be built quite easily by one developer. The ideal end result might not be a separate app or website, but instead it should be part of an existing service such as Google Maps. Unsurprisingly, Google Maps already provides similiar function for single locations, such as gas stations along the route you're currently navigating through.

The project could be developed further by using the planned & realized search/visit history of other users. For example, people who travelled along this route usually visited here and ate there.


## Acknowledgments

Services providing similiar features already exist, such as [Roadtrippers.com](https://roadtrippers.com/), Google Maps and Tripadvisor. However, as of the time of writing the search provided by Google and Tripadvisor are somewhat simplified and Roadtrippers.com requires manual labor for adding stopovers.
