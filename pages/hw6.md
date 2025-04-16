---
layout: default
title: "Homework 6: UFO Sightings with Altair"
permalink: /hw6/
---

#  Homework 5: UFO Sightings with Altair

---

### [The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)  
### [The Analysis Notebook](https://github.com/rithikavennamaneni/RithikaVennamaneni.github.io/blob/main/python_notebooks/Workbook.ipynb)

---

##  Plot 1: UFO Sightings Over Time

<iframe src="/assets/chart1_ufo_time.html" width="700" height="700"></iframe>

This plot visualizes the number of UFO sightings per year. Using the `date_time` column, I extracted the year using `pandas` and grouped the sightings accordingly. The x-axis shows each year, while the y-axis represents the count of sightings. A line chart with dots was used to show year-over-year changes.

For encoding, I used the year on the x-axis and count on the y-axis. I included tooltips to make the chart more interactive, allowing users to hover and view exact values. I used a simple blue line style to maintain clarity.


---

##  Plot 2: Interactive Map of UFO Sightings by Country

<iframe src="/assets/chart2_ufo.html" width="750" height="700"></iframe>

This plot displays UFO sightings using a world map. Each point represents a sighting and is positioned by latitude and longitude. I used a dropdown filter to let users select a country and see sightings specific to that country. The shape of the UFO is encoded using color.

Encodings include longitude on the x-axis, latitude on the y-axis, and color representing UFO shape. I used a dropdown filter with `alt.param()` and `transform_filter()` in Altair v5 to enable interactivity.


---

## Interactivity Discussion

The second plot uses a dropdown to filter sightings by country. This goes beyond default pan/zoom interactions and helps users focus on a specific region’s reports. For example, selecting `us` shows high-density areas, while selecting `gb` reveals patterns in the UK. This makes the visualization more engaging and insightful.
