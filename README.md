# Population_tool_v3
**Population_tool Pt1 build dataset.Rmd** 
This script creates a dataset containing ward level population and deprivation data.

**Population_tool Pt2 build shiny app**
This script reads in the ward level population/deprivation data, and builds a shiny web app to present that data within an interactive tool.
  
# DATA CHARACTERISTICS
* single year of age  
* split by persons/males/females  
* count of people in that age/sex group per ward  
* count of people in that age/sex group per ward who live in the 10% most deprived areas  
* count of people in that age/sex group per ward who live in the 20% most deprived areas  
* count of people in that age/sex group per ward who live in the 30% most deprived areas  

# METADATA  

| Field | Desc |
|-----------------------------------|----------------------------------|
|Popn_estimate_source               | Refers to the ONS table which this data comes from. Included to provide an audit trail  |  
| LAD18CD                           | ONS code for the Local Authority  |  
| LAD18NM                           | ONS name for the Local Authority  |  
| WD18CD                            | ONS code for the Ward  |  
| WD18NM                            | ONS name for the Ward  |  
| Year  |   |  
| Age   |   |  
| Sex   | 'Persons', 'Males', or 'Females'  |  
| Count | The estimated number of people in that age/sex/ward group |  
| Count_in_IMD2015_decile_1 | The estimated number of people in that age/sex/ward group who live in IMD decile 1, the 10% most deprived areas in England    |  
| Count_in_IMD2015_decile_1_to_2 | The estimated number of people in that age/sex/ward group who live in IMD decile 1 or 2, the 20% most deprived areas in England    |  
| Count_in_IMD2015_decile_1_to_3 | The estimated number of people in that age/sex/ward group who live in IMD decile 1,2 or 3, the 30% most deprived areas in England    |  


# DATA SOURCES  

**Desc:** ONS supplied Small area mid year popuykation estimates for 2017  
**Source:** https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/lowersuperoutputareamidyearpopulationestimates  
**Notes:** Download the unformatted version (SAPE20DT2), which is easier to read into R. I've never worked out why, but after unzipping the file I can't read the .xls into R. The workaround is to open the unzipped file in Excel, save it as .xls  

**Desc:** ONS supplied lookup between LSOA and ward/Local Authority  
**Source:** http://geoportal.statistics.gov.uk/datasets/interim-lower-layer-super-output-area-2011-to-ward-to-lad-may-2018-lookup-in-england-and-wales  
**Direct link to csv:** https://opendata.arcgis.com/datasets/5f30206c6fe0402395681b84910d79e9_0.csv
**Notes:** We can read this directly in, no need to download the file first  

**Desc:** English indices of deprivation 2015  
**Source:** https://www.gov.uk/government/statistics/english-indices-of-deprivation-2015  
**Direct link to csv:** https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/467774/File_7_ID_2015_All_ranks__deciles_and_scores_for_the_Indices_of_Deprivation__and_population_denominators.csv  
**Notes:** We can read this directly in, no need to download the file first  

