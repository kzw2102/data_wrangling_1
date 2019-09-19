Data Import
================
Kelly Wang
9/17/2019

## Load in a dataset

``` r
##reads in a dataset
litters_data=read.csv(file ="./data/FAS_litters.csv")
litters_data=janitor::clean_names(litters_data)
```

\#load in pups data

``` r
pups_data=read_csv(file="./data/FAS_pups.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   `Litter Number` = col_character(),
    ##   Sex = col_double(),
    ##   `PD ears` = col_double(),
    ##   `PD eyes` = col_double(),
    ##   `PD pivot` = col_double(),
    ##   `PD walk` = col_double()
    ## )

``` r
pups_data=janitor::clean_names(litters_data)
```

\#\#play with column types litters\_data = read\_csv( file =
“./data/FAS\_litters.csv”, col\_types = cols( Group =
col\_character(), `Litter Number` = col\_character(), `GD0 weight` =
col\_double(), `GD18 weight` = col\_double(), `GD of Birth` =
col\_integer(), `Pups born alive` = col\_integer(), `Pups dead @ birth`
= col\_integer(), `Pups survive` = col\_integer() ) )
tail(litters\_data)

\#\#read in an excel file

``` r
library(readxl)

mlb11_data=read_excel(path="./data/mlb11.xlsx")
#only if you just want a subset of the excel sheet
mlb11_data_subset=
  read_excel(
    path="./data/mlb11.xlsx",
    range="A1:A77"
  )
```

\#\#read in SAS…

``` r
pulse_data=haven::read_sas("./data/public_pulse_data.sas7bdat")
```

\#exporting dataset

``` r
write_csv(mlb11_data_subset, path = "./data/mlb11_subset.csv")
```
