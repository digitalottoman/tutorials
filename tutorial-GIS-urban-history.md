---
title: GIS for Ottoman Urban History
author: Will Hanley, from Lex Berman
date: 2016-06-23
tags: gis, urban
---

Street shapes and buildings and street and neighborhood names change over time. In order to map past places, often we need to work with maps of the past. This tutorial describes a workflow for scholars doing urban history of particular cities.

# 1. Get QGIS

Download QGIS [here](http://qgis.org/en/site/forusers/download.html). For Mac, be sure to use the [KyngChaos version](http://www.kyngchaos.com/software/qgis), using the instructions it contains.

# 2. Get base maps

Georeferenced historical maps of Middle Eastern cities are available at various sites. A partial list appears below. If you have items to add to this list, add a comment to this tutorial.

City|Year(s)|Map name
---|---|---
**Alexandria**|1898|[Goad](https://earthworks.stanford.edu/?utf8=%E2%9C%93&per_page=10&q=alexandria+egypt)
**Cairo**|1905|[Goad](https://earthworks.stanford.edu/?utf8=%E2%9C%93&q=cairo+egypt+fire+insurance)
**Istanbul**|1882|[Stolpe](https://earthworks.stanford.edu/catalog/harvard-g7434-i8-1882-s86)

# 3. Get shape files for your city

BBBike.org, a site that helps people to plan cycling routes, offers Open Street Maps shape files the following cities:

[Alexandria](http://download.bbbike.org/osm/bbbike/Alexandria/), [Baghdad](http://download.bbbike.org/osm/bbbike/Baghdad/), [Beirut](http://download.bbbike.org/osm/bbbike/Beirut/), [Cairo](http://download.bbbike.org/osm/bbbike/Cairo/), [Istanbul](http://download.bbbike.org/osm/bbbike/Istanbul/), [Jerusalem](http://download.bbbike.org/osm/bbbike/Jerusalem/),
[Tehran](http://download.bbbike.org/osm/bbbike/Tehran/)

Download the `yourcityname.osm.shp.zip` file.

# 4. Choose your data fields

You'll want to figure out which data fields you want to use to enter your data.
