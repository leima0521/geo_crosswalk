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
