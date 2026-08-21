# I-15 PeMS Station Analysis

This project uses Caltrans PeMS data to evaluate traffic conditions on I-15 in San Diego County, with a focus on comparing managed/express lane performance with nearby general purpose lanes.

## Project Overview

The analysis:

- Reads and cleans District 11 PeMS station-hour data.
- Identifies healthy stations based on data completeness.
- Matches managed lane stations with nearby general purpose lane stations.
- Compares speeds and traffic volumes by direction and time of day.
- Produces tables and maps for reporting.

## Main Files

### create_master_data.R

Creates the master PeMS dataset used for the analysis.

The script:

- Reads monthly PeMS station-hour files.
- Reads PeMS station metadata.
- Filters to I-15 northbound and southbound stations.
- Adds station location information.
- Creates data-quality flags.
- Saves the cleaned master dataset.

### PeMS Analysis.R

Performs the main analysis.

The script:

- Evaluates station health.
- Selects usable managed lane and general purpose stations.
- Matches managed lane stations to nearby general purpose stations.
- Calculates speed and volume measures.
- Produces comparison tables and maps.

### PeMS Analysis - Working Notes.docx

Working documentation describing the methodology, assumptions, and results.

## Data

Raw PeMS data are not stored in this repository because of file size.

The project expects source data to be stored locally in:

`1_Source Data/PeMS Station Data/`

PeMS station metadata should be stored under:

`1_Source Data/`

## R Packages

The analysis uses packages including:

- tidyverse
- janitor
- lubridate
- writexl
- sf
- ggplot2
- ggrepel

## Status

Work in progress.
