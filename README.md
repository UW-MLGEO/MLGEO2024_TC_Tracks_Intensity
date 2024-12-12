# Tropical Cyclone Tracking and Intenity (Alton Daley)


The URL of this Repository can be found [URL](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity). The repository consist of a data, notebook and script directory. The 

## Data Source

The best track and SHIPS data can be retrieved from  [NCEI-NOAA](https://www.ncei.noaa.gov/data/international-best-track-archive-for-climate-stewardship-ibtracs/v04r01/access/csv/ibtracs.NA.list.v04r01.csv) and [RAMMB2-CIRA](https://rammb-data.cira.colostate.edu/ships/data/AL/lsdiaga_1982_2023_sat_ts_7day.txt) respectively. A compressed verion of the data can be found [here](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/tree/dev/data/raw). The metadata information for the best track and SHIPS data can be found at [IBTRacs](https://www.ncei.noaa.gov/sites/g/files/anmtlf171/files/2024-07/IBTrACS_version4r01_Technical_Details.pdf) and [SHIPS](https://rammb-data.cira.colostate.edu/ships/data/ships_predictor_file.pdf)

The data can be converted to a .csv file using the [Notebook](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Download_Data.ipynb). 

## Project Objectives

Tropical Cyclones are natural disaster that cause severe imapcts to coastal communities. At the coast these impacts are manifested as extreme rain, wind and storm surge. It is important to provide these commuties with accurate storm tracks and intensity (peak winds and minimum sea level pressure) before these storms make landfall. With this in mind the objectives of this project are to :
-   develop a forecast model to predict Tropical Cyclone Tracks up to 24 hr.
-   Forecsat peak wind speeds up to 24 hrs ahead.
-   Detect the occurence of Rapid Intensification

## Description of each notebook

The repository consist of 4 notebooks. The notebooks performs the following function:

- [Download_Data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Download_Data.ipynb), Retrives the raw data from [raw data folder](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/raw/raw_data.tar.gz)

- [clean_ibtracs_data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/clean_SHIPS_data.ipynb), cleans up the best track data and produces the [cleaned_best_track_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/clean/cleaned_best_track_data.csv) file.

- [clean_SHIPS_data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/clean_SHIPS_data.ipynb), cleans up the SHIPS data and produces the [cleaned_SHIPS_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/clean/cleaned_SHIPS_data.csv) file.

- [Prepare_AI_Ready_Data.ipynb](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/notebooks/Prepare_AI_Ready_Data.ipynb), creates the AI Ready Data a csv file [ai_ready_SHIPS_data.csv](https://github.com/UW-MLGEO/MLGEO2024_TC_Tracks_Intensity/blob/dev/data/ai_ready/ai_ready_SHIPS_data.csv) file.

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

### Running the Data Download Script

To run the notebook:
- Import the appropriate libraries 
- Run the Reading and Extracting Data code block, which will extract the SHIPS and IBTracs data.
- The data will be downloaded to your current directory. Move the data file to the ```data\raw``` directory.

### Running the Data Cleaning Script

- Import the appropriate libraries 
- Run the Reading Data code block to open the ```lsdiaga_1982_2022_sat_ts_5day.txt``` file.
- Execute the next code block, which consists of a series of functions to help extract the data of interest. 
- Run the next code block to create empty arrays for storing the data of interest.
- Extract the data using the functions from the Function code block.
- Execute the Clean Up Data code block which removes outliers, converts units, and invalid entries to ```NaNs```
- Create the dataframe using the Create Dataframe code block. This code block also ensures that the data is cleaned appropriaely

### Running the Prepare AI Ready Data

- Import the appropriate libraries
- Set File PATHS and open file with the first code block
- The notebook provides a list of all the features in the data
- Execute the next code block to select the most meaningful data

### Running the Exploratry Data Analysis
- Import the appropriate libraries
- Ensure file paths are set apprpriately
- Investigate basic statistics of the data (min, max, mead, stdev) using the 4th code block
- Execute the next code block to visualize the distribution of the features
- Investigate the correlation of features by executing the final two code blocks


### Running the Dimentionality Reduction

- Import the appropriate libraries
- Ensure file paths are set apprpriately
- Visualize the firstfew columns
- Remove unwanted data with the next code block
- Perform PCA analysis with the next 3 code block 
    - The first investigates all the data and the remaining two is specific to storm intensity and TC tracking
- Perform the t-Distributed Stochastic Neighbor Embedding (t-Distributed Stochastic Neighbor) with the remaining script ()





