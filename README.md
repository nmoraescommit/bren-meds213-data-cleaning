# Cleaning the shorebird survey data 


## The data set

ARCTIC SHOREBIRD DEMOGRAPHICS NETWORK [https://doi.org/10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W)

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the [course data repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-spring-2024-class-data) for full metadata information about this data set.

## DATA & FILE OVERVIEW

1. File List:
 - data folder: contains raw and processed data for the project
  - processed folder
   - snow_survey_fixed.csv: Cleaned records of species (birds and mammals) encountered during field work each day at each site via the code in data_cleaning.qmd.
   - species_presence.csv: Cleaned records of snow cover remaining at the site via the code in data_cleaning.qmd.
  - raw folder
    - ASDN_Daily_species.csv: Record of the species (birds and mammals) encountered during field work each day at each site
    - ASDN_Snow_survey.csv: Periodic records of snow cover remaining at the site
    - 01_ASDN_Readme.txt: See "01_ASDN_readme.txt" for detailed data author and contact information.
 - docs folder: Contains web assets and libraries to render HTML documentation.
  - data_cleaning_files
    - libs
      - bootstrap: styling
      - clipboard: copy-to-clipboard functionality
      - quarto-htm: core HTML rendering features
 - data_cleaning.qmd
 - README.md

2. Relationship between files, if important:

The .csv's in the raw folder are read in and processed within the the data_cleaning.qmd - which is directed to create snow_survey_fixed.csv and species_presence.csv.

3. Additional related data collected that was not included in the current
data package:

NA

4. Are there multiple versions of the dataset? 
This data set is hosted on [NSF Artic Data Center](https://arcticdata.io/catalog/view/doi%3A10.18739%2FA2222R68W) - and has been published in 2016 - it is the only version hosted on the site and the version we are using in this project.

## DATA-SPECIFIC INFORMATION FOR:

For the file  data/processed/all_cover_fixed_EvaNewby.csv : 

1. Number of variables: 11

2. Number of cases/rows: 42,830

3. Variable List: <list variable name(s), description(s), unit(s)and value 
labels as appropriate for each>
- Site: ASDN field sites are referred to by 4-letter codes in each of the data files.  General information on each site is given here.  Not all types of data are available for every site.
- Year: YYYY Format, Year in which data were collected.
- Date: Date of capture.
- Plot: Study plot name.
- Location: Unique site location identification code.
- Snow_cover: Percent cover of snow, including slush.
- Water_cover: Percent cover of water.
- Land_cover: Percent cover of exposed land.
- Total_cover:	Total sum (to check the above percents; should always sum to 100).
- Observer:	Person who conducted the survey.
- Notes:  Free-text field for relevant comments or contextual information from the field.

5. Missing data codes: <list code/symbol and definition>
-    NA: Not applicable or not available.
-    Blank, "" or "-" : No data recorded.

7. Specialized formats or other abbreviations used:
- Site: A standardized four-letter code indicating the ASDN field site where data were collected (e.g., barr, nome, east). Each code corresponds to a specific geographic location
- Date: Recorded in YYYY-MM-DD ISO format. Represents the exact day of the survey or observation.
- Plot: Name or code of the study plot within the field site where the survey occurred. Plot names may include numeric or alphanumeric identifiers and are unique within each site.
- Location: A unique location identifier within the plot or site, used to distinguish between different micro-sites, subplots, or snow survey transects. May be used for repeated measurements over time.
- Snow_cover, Water_cover, Land_cover: Visual estimates of percent surface cover (0–100%) for snow/slush, standing or pooled water, and exposed land, respectively. These fields are expected to be mutually exclusive and collectively exhaustive.
- Total_cover: The sum of the three cover types (Snow_cover, Water_cover, and Land_cover), which must equal 100.
- Observer: Person who conducted the survery, listed as first initial followed by last name. For example: Naomi Moraes would be "nmoraes".

## SHARING/ACCESS INFORMATION

1. Licenses/restrictions placed on the data: The data used in this project is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.

2. Links to publications that cite or use the data:
All 16 uses of this data being cited can be found in the "Citations" link in the [host site](https://arcticdata.io/catalog/view/doi%3A10.18739%2FA2222R68W). Some example publication that cite the data are:
- https://onlinelibrary.wiley.com/doi/10.1111/gcb.17356
- https://link.springer.com/article/10.1007/s10646-023-02708-w
- https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0270957

3. Links to other publicly accessible locations of the data:

- [DataONE.org](https://search.dataone.org/view/doi:10.18739%2FA2222R68W): https://search.dataone.org/view/doi:10.18739%2FA2222R68W

4. Links/relationships to ancillary data sets: <any supplementary data sources 
that support analysis or classification of the datasets, eg., plant taxonomy table.)>

This dataset is part of the Arctic Shorebird Demographics Network (ASDN) and is related to several ancillary data files that provide supporting information:
- site.csv – Provides full names, geographic locations, and metadata for each 4-letter ASDN site code.
- personnel.csv – Contains information on field observers, including full names, affiliations, and dates of site involvement.
- Study_Plot (KMZ) – Google Earth-compatible file showing the spatial boundaries of plots referenced in the Plot and Location fields.
- Snow_survey.csv (raw version) – The original source file for snow, water, and land cover observations before processing and formatting.

6. Was data derived from another source? If yes, list source(s): <list citations 
to original sources>
- This processed dataset (all_cover_fixed_NaomiMoraes.csv) was derived from the raw ASDN Snow_survey data file.
- The original source is: Arctic Shorebird Demographics Network. "ASDN_Snow_survey.csv" (1993–2014). NSF Arctic Data Center. https://arcticdata.io

7. Recommended citation for the project:
- Lanctot, R.B., Brown, S.C., and Sandercock, B.K. (2017). Arctic Shorebird Demographics Network. NSF Arctic Data Center. [https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W]