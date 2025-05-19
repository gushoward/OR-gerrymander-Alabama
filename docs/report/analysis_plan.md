# Gerrymandering in Alabama

### Authors

- Augustus Howard\*, augustush@middlebury.edu, @gushoward, github.com/gushoward, Middlebury College


### Abstract

This study investigates the p extent of gerrymandering in the state of Alabama by employing a multidimensional approach. We evaluate three shape-based compactness metrics to assess the geometric integrity of district boundaries. Additionally, we analyze the representativeness of electoral districts by comparing them against historical presidential election results and racial demographics, providing insights into potential partisan and racial gerrymandering. Expanding upon previous research, we use an additional metric that calculates representativeness using the convex hulls of district polygons, offering a new perspective on spatial fairness. This reproduction aims to build upon existing findings while contributing a methodological refinement to the study of gerrymandering.

This is an original study based on gerrymandering literature. It is an exploratory investigation into the value of varied convex hull methods to assessing gerrymandering.

## Study Metadata

- `Key words`: Gerrymandering, convex hull, Alabama, compactness, political representation
- `Subject`: Social and Behavioral Sciences: Geography: Geographic Information Sciences
- `Date created`: 2025-02-17
- `Date modified`: 2025-02-17
- `Spatial Coverage`: Alabama OSM:[161950](https://www.openstreetmap.org/relation/161950)
- `Spatial Resolution`: Census Block Groups
- `Spatial Reference System`: EPSG: 4269 NAD 1983 Geographic Coordinate System
- `Temporal Coverage`: 2020-2024 population and voting data
- `Temporal Resolution`: Decennial Census



## Study design

This is an original study based on literature on gerrymandering metrics.

It is an exploratory study to evaluate the usefulness of a new gerrymandering metric based on
the convex hull of a congressional district and the representativeness inside the convex hull compared to the congressional district.

## Materials and procedure

### Computational environment

I plan on using package the following packages: tidyverse - for general data manipulation, here - for file location, sf - for analyzing spatial data, tmap - to represent spatial data, tidycensus - for gathering census data, and kableExtra with R version 4.4.2.

packages <- c("tidyverse",
              "here",
              "sf",
              "lwgeom",
              "tmap",
              "tidycensus",
              "knitr", 
              "htmltools",
              "markdown")

# the following date is used to determine the versions of R and the packages used.

groundhog.day <- "2025-02-01"           
### Data and variables

### Block Groups
- `Title`: Block Groups 2020
- `Abstract`: Vector polygon geopackage layer of 2020 Census Block Groups and demographic data
- `Spatial Coverage`: Alabama
- `Spatial Resolution`: Census Block Groups
- `Spatial Reference System`: EPSG 4269 NAD 1983 geographic coordinate system
- `Temporal Coverage`: 2020 Census
- `Temporal Resolution`: 2020 Census
Block Groups
- GEOID: code to uniquely identify tracts
- P4_001N: Total Population, 18 years or older
- P4_006N: Total: Not Hispanic or Latino, Population of one race, Black or African American alone, 18 years or older
- P5_003N:Total institutionalized population in correctional facilities for adults, 18 years or older

### Districts
- `Title`: Voting Districts 2020
- `Abstract`: Congressional Districts
- `Spatial Coverage`: Alabama
- `Spatial Resolution`: US Congressional Districts
- `Spatial Reference System`: EPSG 3857 WGS 1984 Web Mercator projection
- `Temporal Coverage`: Districts approved in 2023 for 2024
- `Temporal Resolution`: annual election

US Congressional districts
- DISTRICT: US Congressional District Number
- POPULATION: Total Population (2020 census)
- WHITE: total white population (2020 census)
- BLACK: total Black or African American population (2020 census)


**Standard Metadata**

The metadata files can be found in data/metadata

## Prior observations  

At the time of this study pre-registration, the author had little prior knowledge of the geography of the study region with regards to the gerrymandering phenomena to be studied.
This study is related to one prior study by the author, in which the compactness of Alabama's voting districts was calculated, as well as voting statistics in relation to race.

## Bias and threats to validity

MAUP and Scale may affect these results.

Given the boundaries of this study are essential to the analysis, the Modifiable Areal Unit problem will certainly have relevant impacts. The constantly changing boundaries of voting precincts can impact both visualization of the data, as well as the analysis of it. The scale and shape of the units used has the potential to alter the data used in the study.

### Data transformations

Calculate Percent Black. Transform block groups to WGS 1984 projection.


### Analysis

The results will be mapped and compactness of regions will be calculated in order to understand the effects of gerrymandering in Alabama.



## Integrity Statement

The authors of this preregistration state that they completed this preregistration to the best of their knowledge and that no other preregistration exists pertaining to the same hypotheses and research.
If a prior registration *does* exist, explain the rationale for revising the registration here.


This report is based upon the template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences, DOI:[10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)
