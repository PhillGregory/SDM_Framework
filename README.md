# SDM-XAI-Framework

## Overview
This repository consists of a diagrammatic Species Distribution Modelling (SDM) framework pdf and example implementations of each stage in the flow chart. Existing species occurrence and environmental data has been sourced online and saved into the 'datasets folder. For the purpose of this IT artefact, the data contains tiger species occurrence data for the year 2023 along with the associated environmental data. The environmental data is taken for the year 2023 in India.

The diagrammatic SDM framework pdf file provides a flow chart of development steps with the end goal of producing an interpretable SDM by levraging domain knowledge. The overall IT artefact demonstrates how data can be sourced, processed, modelled, and interpreted. The "MaxEnt_Tigers_In_India.ipynb" provides code that can be used and adapted for creating MaxEnt species distribution models. In reality, the development flow would incorporate a domain expert at each developmental stage, as shown in the Species Distribution Modelling (SDM) framework pdf.

## Structure
The repository is structured as below:
```
SDM_FRAMEWORK
├── MaxEnt : This folder contains the MaxEnt open source software along with the MaxEnt README. 
├── MaxEnt_Tigers_in_India.ipynb : Example SDM implementation using Python
├── README.md : This repository README file
├── SDM Framework.pdf : Diagrammatic SDM framework
├── datasets : The tiger occurrence and environmental datasets from online sources
├── layers : Environmental layers for use in MaxEnt
├── outputs : Output files of the MaxEnt model
├── references : References for the utilised publications, software, and datasets
├── requirements.txt : Installation requirements
├── samples : Clean tiger occurrence data for use in MaxEnt
└── venv : Virtual environment used for this project
```

## Installation instructions

1. Clone this repository with the below command:
git clone https://github.com/PhillGregory/SDM_Framework.git

2. Create and activate a virtual environment
**MACOS/LINUX commands**
python3 -m venv venv
source venv/bin/activate

**Windows commands**
python -m venv venv
.\venv\Scripts\activate

3. Install the dependencies to your virtual environment which are stored in the requirements.txt file:
pip install -r requirements.txt

4. The MaxEnt software is located in the 'MaxEnt' folder and is called maxent.jar. As per the 'MaxEnt README', Windows users can open the software using 'maxent.bat'. Mac and Linux users can use the below command:
java -jar /path/to/maxent/maxent.jar  (Replace the file path as appropriate)

## Data source information
**Tiger species occurence data:**
This data was sourced from the Global Biodiversity Information Facility: https://www.gbif.org. To obtain the tiger_occurrence_data.csv file, I used the "occurrences" page and then used the below filter options:
* Country or area: India
* Scientific name: Panthera tigris (Linnaeus, 1758)
* Year: 2019 - 2023
* Reference: GBIF.org. GBIF Occurrence Download. Available at: https://doi.org/10.15468/dl.sgeq2r. (Accessed 3 September 2024)

The above filters can easily be used in real use-cases to extract species occurrence data relevant to the project requirements.

**Environmental data**
This data was sourced from the Climate Data Store (CDS): https://cds-beta.climate.copernicus.eu. To obtain the ERA5_environmental_data.nc file, I selected "ERA5-Land monthly averaged data from 1950 to present" as this dataset allowed me to extract land environmental features filtered to the same spatial and temporal range as the tiger species occurrence data. The data request criteria is below:
* Product type: Monthly averaged reanalysis by hour of day
* Variables: 2m dewpoint temperature, 2m temperature, Surface solar radiation downwards, Runoff, Total evaporation, 10m u-component of wind, 10m v-component of wind, Total precipitation, Leaf area index, high vegetation
* Year: 2019 - 2023
* Month: All months
* Time: 12:00pm
* Geographical area: North: 37°, West: 68°, South: 8°, East: 97° (India)
* Data format: NetCDF4
* Reference: Muñoz Sabater, J. (2019): ERA5-Land monthly averaged data from 1950 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS). DOI: 10.24381/cds.68d2bb30 (Accessed on 3 September 2024)

## License information
Using the MaxEnt open source software for publication, report, or online posting requires the below citation:
Steven J. Phillips, Miroslav Dudík, Robert E. Schapire. (No date). Maxent software for modeling species niches and distributions (Version 3.4.1). Available from url: http://biodiversityinformatics.amnh.org/open_source/maxent/ (Accessed on 3 September 2024)

## Project conclusion
This repository has provided a suggested approach for creating SDMs to leverage domain knowledge and explainable AI (XAI) in the form of a pdf framework. The supporting Juptyer notebook allowed me to act as a data scientist in the absence of a domain expert and a project manager and supported my hypotheses that model development could be improved using these additional stakeholders. As expected, the areas that would be most benefitted from domain experts and project managers where at the beginning and ends of the project. Namely, requirements gathering, data collection, and model interpretation.

Despite not having access to domain expertise or a project manager, I was able to produce a MaxEnt SDM that predicts tiger occurrences in India based on real world data from the years 2019 - 2023. The model had good predictive power with an AUC of 0.799 and it was revelaed that the most important variable was "Leaf Area Index High Vegetation". This aligns with ecological expectations that tigers would prefer leafy jungle-like habitats.

## Project and contact details
* This repository was created in conjunction with a dissertation report which will serve as my capstone project for the Computer Science MSc course
* Contact email: p.gregory@liverpool.ac.uk