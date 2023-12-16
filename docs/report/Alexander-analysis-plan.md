---
title: "Alexander-analysis-plan.md"
author: "Sydney Alexander"
date: "2023-11-09"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Planned revsions to reproduction of

Author: Sydney, Alexander

## Analysis + Rationale

Our planned modifications include the following: we will improve speed limit information by replacing the `network_setting` function iwth use of the `osmnx.speed` module.
We will also improve translation of hospital catchments into hexagons by modifying the `overlap_calc` function.
Instead of exlcuding hospital catchments whose area is less than 50% within a certain hexagon, we will weight the service area by the percentage of overlap.
we will comment every line of the ***overlap_calc*** function in order to improve readibility and comprehension.

## Results

The code for setting speed limits of the streets will be much more concise and efficent by using the `osmnx.speed` module.
The visualization of the Accessibility Map will change, as hexagons will be weighted differently, taking into account the area of overlap between the hexagons and the catchment areas. 
