# SDM-XAI-Framework

## Overview
This repository consists of a diagrammatic Species Distribution Modelling (SDM) framework pdf and example implementations of each stage in the flow chart. Existing species occurrence and environmental data has been sourced online and saved into the 'datasets folder. For the purpose of this IT artefact, the data contains tiger species occurrence data for the year 2023 along with the associated environmental data. The environmental data is taken for the year 2023 in India.

The diagrammatic SDM framework pdf file provides a flow chart of development steps with the end goal of producing an interpretable SDM by levraging domain knowledge. The overall IT artefact demonstrates how data can be sourced, processed, modelled, and interpreted. In reality, the development flow would incorporate a domain expert at each developmental stage, as shown in the Species Distribution Modelling (SDM) framework pdf.

## Structure
The repository is structured as below:

INSERT STRUCTURE HERE

## Installation instructions

INSERT INSTALLATION INSTRUCTIONS HERE

## Data source information
**Tiger species occurence data:**
This data was sourced from the Global Biodiversity Information Facility: https://www.gbif.org. To obtain the tiger_occurrence_data.csv file, I used the "occurrences" page and then used the below filter options:
* Country or area: India
* Scientific name: Panthera tigris (Linnaeus, 1758)
* Year: 2023
* Citation: GBIF.org (26 August 2024) GBIF Occurrence Download  https://doi.org/10.15468/dl.3tcxf5

For this example, the data was isolated to India and 2023 to limit the sample size. However, the filters can easily be used in real use-cases to extract species occurrence data relevant to the project requirements.

**Environmental data**
This data was sourced from the Climate Data Store (CDS): https://cds-beta.climate.copernicus.eu. To obtain the ERA5_environmental_data.nc file, I selected "ERA5-Land monthly averaged data from 1950 to present" as this dataset allowed me to extract land environmental features filtered to the same spatio and temporal range as the tiger species occurrence data. The data request criteria is below:
* Product type: Monthly averaged reanalysis by hour of day
* Variables: 2m dewpoint temperature, 2m temperature, Surface solar radiation downwards, Runoff, Total evaporation, 10m u-component of wind, 10m v-component of wind, Total precipitation, Leaf area index, high vegetation
* Year: 2023
* Month: All months
* Time: 12:00pm
* Geographical area: North: 37°, West: 68°, South: 8°, East: 97° (India)
* Data format: NetCDF4
* Citation: Muñoz Sabater, J. (2019): ERA5-Land monthly averaged data from 1950 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS). DOI: 10.24381/cds.68d2bb30 (Accessed on 26-Aug-2024)

## Conclusion

CONCLUDE WITH A SUMMARY OF THE IT ARTEFACT

## Contact details
Email: p.gregory@liverpool.ac.uk
