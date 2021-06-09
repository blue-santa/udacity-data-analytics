# Analysis of the 2009 Flight Expo Data
## by Bryan Beus


## Dataset

The 2009 Flight Data Expo provides information on flights in Northern America, with a focus on information regarding delays and cancellations.

This investigation observes and studies the AirTime, DepDelay, and Origin features of the provided dataset. 


## Summary of Findings

The `AirTime` values are highly skewed to the right, therefore the logarithmic scale is appropriate for the x-axis. 

The mode appears to be approximately `50` minutes. There appears to be a slight secondary peak in the data at approximatley `200` minutes.

The `DepDelay` values are highly skewed to the right, but many of the values are negative (wherein flights departed ahead of schedule). Therefore, the logarithmic scale is not appropriate for the x-axis. However, the y axis values are too spread out, and therefore a logarithmic scale is more appropriate.

The mode appears to be approximately `10` minutes. 

The five most common origins are LAS (Los Angelos), MDW (Chicago), PHX (Phoenix), BWI (Maryland), and HOU (Houston).

The five least common origins are HRL (Texas), RSW (Florida), IAD (Virginia/DC), JAN (Mississippi), and CRP (Texas).

In the Bivariate exploration, in comparing `DepDelay` against `Origin`, the viewere may note that the three highest origins were all seen previously in the Most Common Origins graph, but the next two  origins were not seen. 

This raises questions about why these two airports are underperforming.

In the Multivariate exploration, `AirTime` and `DepDelay` values are plotted against each other as a scatter plot, and the scatter points are given a hue color according to `Origin`.

A casual glance at the image could lead the viewer to interpret that higher-value departure delays are most often associated with the hue for `MDW`.

