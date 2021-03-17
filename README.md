# Geographic crosswalk files

## State FIPS
[State FIPS folder](https://github.com/leima0521/geo_crosswalk/tree/master/state_fips) includes crosswalk files for state name, state abbreviation, and state FIPS code in .dta and .csv format.
R users can use the `tidycensus` package to get FIPS code at the state and county levels. Here is an example of how to extract state name and FIPS from the file
```
library(tidycensus)
data(fips_codes)
fips_codes <- fips_codes %>%
  transmute(STATEFIP = as.integer(state_code),
            state_name) %>%
  distinct()
```
## County-commuting zone crosswalk
- Crosswalk files by [David Dorn](https://www.ddorn.net/data.htm)
- Crosswalk files by [USDA ERS](https://www.ers.usda.gov/data-products/commuting-zones-and-labor-market-areas/)
- Crosswalk files by [Fabian Eckert, Andrés Gvirtz, Jack Liang, and Michael Peters](http://fpeckert.me/eglp/). [Github repo](https://github.com/liang-jack-a/EGLP_Crosswalk)
