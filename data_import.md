Data Import
================
9/17/2019

## Load in a dataset

``` r
##reads in a dataset
litters_data=read.csv(file = "./data/FAS_litters.csv")
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
