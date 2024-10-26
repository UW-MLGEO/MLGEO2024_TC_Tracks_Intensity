# Tropical Cyclone Tracking and Intenity (Alton Daley)


The URL of this Repository can be found [URL](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity).

## Data Source

The best track and SHIPS data can be retrieved from  [NCEI-NOAA](https://www.ncei.noaa.gov/data/international-best-track-archive-for-climate-stewardship-ibtracs/v04r01/access/csv/ibtracs.NA.list.v04r01.csv) and [RAMMB2-CIRA](https://rammb-data.cira.colostate.edu/ships/data/AL/lsdiaga_1982_2023_sat_ts_7day.txt) respectively. A compressed verion of the data can be found [here](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/tree/dev/data/raw). The metadata information for the best track and SHIPS data can be found at [IBTRacs](https://www.ncei.noaa.gov/sites/g/files/anmtlf171/files/2024-07/IBTrACS_version4r01_Technical_Details.pdf) and [SHIPS](https://rammb-data.cira.colostate.edu/ships/data/ships_predictor_file.pdf)

The data can be converted to a .csv file using the [Notebook](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Download_Data.ipynb). 

## Project Objectives

The objectives of this project is to :
-   develop a forecast model to predict Tropical Cyclone Tracks up to 24 hr, 48 hrs and 72 hrs ahead.
-   Forecsat peak wind speeds and minimum sea level pressure up to 24 hr, 48 hrs and 72 hrs ahead.
-   Detect the occurence of Rapid Intensification

## Description of each notebook

The repository consist of 4 notebooks. The notebooks performs the following function:

- [Download_Data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Download_Data.ipynb), Retrives the raw data from [raw data folder](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/raw/raw_data.tar.gz)

- [clean_ibtracs_data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/clean_SHIPS_data.ipynb), cleans up the best track data and produces the [cleaned_best_track_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/clean/cleaned_best_track_data.csv) file.

- [clean_SHIPS_data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/clean_SHIPS_data.ipynb), cleans up the SHIPS data and produces the [cleaned_SHIPS_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/clean/cleaned_SHIPS_data.csv) file.

- [Prepare_AI_Ready_Data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Prepare_AI_Ready_Data.ipynb), creates the AI Ready Data [ai_ready_SHIPS_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/ai_ready/ai_ready_SHIPS_data.csv) file.

- [EDA.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/EDA.ipynb), explores the distribution and correlation of features in the AI Ready Data.

- [Dimentionality_Reduction.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/EDA.ipynb), explores the distribution and correlation of features in the AI Ready Data.

## Installing the Repository
```
git clone https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity.git
conda env create -f environment.yml
conda activate mlgeo_dataset
```


## Running the Notebooks

### Setting Up Conda Environment
- Running `conda env create -f environment.yml` should create the environment and install the required modules.
- Select the `mlgeo_dataset` environment

To run the notebook:
- Install Python and create the mlgeo_dataset conda environment.
- Run cells in the order given (Ensure that you change the PATH to directory storing the PNG file)

## Favorite Earth Sciences Topics

- Renewable Energy Sources
- Tropical Cyclones
- Air-Sea Interaction
- Coupled Atmosphere-Wave-Ocean Modelling
- Coastal Environment and Climate Change

## Licensing

I decided to use the MIT licensing because it is:

- Simple
- Premissive
- Promotes collaboration
