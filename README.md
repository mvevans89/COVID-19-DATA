# COVID-19-DATA

Repository that stores datasets used in different projects 
=======

# Contact

John Drake (jdrake@uga.edu)

### Folder Code
Stores .R and .Rmd files that generate some of the data files.

#### - read_UScases_wikipedia.R
Extracts data from [2020 coronavirus pandemic in United States wiki page](https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_the_United_States) and outputs file 'UScases_by_state_wikipedia.csv'.

#### - get_world_data.Rmd
Extracts data from [2020 coronavirus pandemic wiki page](https://en.wikipedia.org/wiki/2019%E2%80%9320_coronavirus_pandemic) and adds the current day to the dataset. Must be run every day at ~10 PM or extracted from archived pages on wayback machine.

### Data Files

#### - UScases_by_state_wikipedia.csv
Reads from wikipedia the number of non-repatriated COVID-19 cases in the US by state. Generated by `read_UScases_wikipedia.R`.

##### Metadata:
- `Date` - Date correspondent to the number of cases
- Columns 2-14: Western US states
- Columns 15-27: Midwestern US states
- Columns 28-39: Southern US states
- Columns 40-51: Northeastern US states
- Column 52: GU: Guam, U.S territory
- Column 53: PR: Puerto Rico, U.S territory
- Column 54: VI: United States Virgin Islands, U.S territory
- `Conf_New`: Number of new confirmed cases 
- `Conf_Cml`: Cumulative number of confirmed cases
- `Death_New`: Number of new deaths
- `Death_Cml`: Cumulative number of deaths
- `Rec_New`: Number of new recoveries
- `Rec_Cml`: Cumulative number of recoveries
- `time_last_update`: day and time of last table update


#### - worldCases.csv
Stores data read from wikipedia on the cumulative number of cases in a country. Added to each day by running `get-world-data.Rmd`. Wikipedia does not store these data by date so running daily at the same time is necessary to keep data current and accurate.

##### Metadata: 
 - `Date`: Date of cumulative case record
 - `Country`: Country name
 - `Cases`: cumulative number of cases for `Country` on `Date`

