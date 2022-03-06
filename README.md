# agera5
## An R package for downloading and extracting data from the Copernicus AgERA5 dataset


## Description 

The R package *agera5* is a toolbox to download and extract data from the "Agrometeorological indicators from 1979 to present derived from reanalysis" dataset (aka AgERA5).

https://cds.climate.copernicus.eu/cdsapp#!/dataset/10.24381/cds.6c68c9bb?tab=overview

The download function provides programmatic access to the Copernicus Climate Data Store to download
AgERA5 data.

## Data license
The agera5 package does not distribute data, it only provides access to Climate Data Store through the 
python cdsapi.

For specific details about the license agreenment on downloading and using the data please check the license at: 
https://cds.climate.copernicus.eu/api/v2/terms/static/licence-to-use-copernicus-products.pdf

### Installation  
``` r
devtools::install_github("agrdatasci/agera5", build_vignettes = TRUE)
```
### Downloading AgERA5 data
#### csdapi setup

#### Example
The following example downloads daily 2m_temperature data for year 2015
``` r
download_agera5(agera5_var = "2m_temperature",
                agera5_stat = "night_time_minimum",
                day = "all",
                month = "all",
                year = 2015,
                path = "C:/custom_target_folder"
)
``` 
## Acknowledgements
The *agera5* package relies on the functionality available from other open source packages.

* The Python cdsapi https://pypi.org/project/cdsapi/

* The package *reticulate* is used to access the Python cdsapi functions from R.

* The R package *terra* is used to extract data from nc files.

* The package *fs* is used for efficiently search and list files.


### Disclaimer
Please be aware that is still a development version of the package. You are free to use it for your own purposes with no warranty.

