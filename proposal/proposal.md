Project proposal
================
Team name

``` r
library(tidyverse)
library(broom)
library(here)
```

*For instructions on what each section should include, please see the
[project page](https://idsed.digital/assessments/project/#proposal) on
the course website. Remove this text when completing your proposal*.

## 1. Introduction

Our general research question: Is their a link between dying by the
police and being innocent? The dataset that was downloaded for this
project is from a website called Kaggle and the data in the dataset
comes from a website called Fatal Encounters. They have 3 main ways that
they collect the data. The first way they collect the data is paying
researchers, and around 85% of their data comes from these reliable and
trusted researchers in the data. The second way they collect data is
from Public Record Requests, and the third is from crowd sourced data
which is filtered throughly to accurately report everything.

The variables that we are going to be using is going to be every single
one except for the URL of image, location of injury (address), location
zip code, full address, URL Temp, Brief Description, Supporting Document
Link, Longitude, and Latitude. This would mean we have 18 variables in
total to work with.

## 2. Data

<<<<<<< HEAD
glimpse(head(Innocent\_Deaths\_caused\_by\_Police\_All\_time\_))
=======
    ## Warning: One or more parsing issues, see `problems()` for details

    ## Rows: 30860 Columns: 27

    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (21): Name, Gender, Race, URL of image, Date of injury resulting in deat...
    ## dbl  (5): Unique ID, Age, Location of death (zip code), Latitude, Longitude
    ## lgl  (1): URL Temp

    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    ## # A tibble: 6 × 27
    ##   `Unique ID` Name                    Age Gender Race  `URL of image` `Date of injury…
    ##         <dbl> <chr>                 <dbl> <chr>  <chr> <chr>          <chr>           
    ## 1       25747 Mark A. Horton           21 Male   Afri… <NA>           1/1/2000        
    ## 2       25748 Phillip A. Blurbridge    19 Male   Afri… <NA>           1/1/2000        
    ## 3       25746 Samuel H. Knapp          17 Male   Euro… <NA>           1/1/2000        
    ## 4       25749 Mark Ortiz               23 Male   Hisp… <NA>           1/1/2000        
    ## 5           1 LaTanya Janelle McCoy    24 Female Afri… <NA>           1/2/2000        
    ## 6           2 Lester Miller            53 Male   Race… <NA>           1/2/2000        
    ## # … with 20 more variables: Location of injury (address) <chr>,
    ## #   Location of death (city) <chr>, State <chr>,
    ## #   Location of death (zip code) <dbl>, Location of death (county) <chr>,
    ## #   Full Address <chr>, Latitude <dbl>, Longitude <dbl>,
    ## #   Agency or agencies involved <chr>, Highest level of force <chr>,
    ## #   Alleged weapon <chr>, Aggressive physical movement <chr>,
    ## #   Fleeing/Not fleeing <chr>, Description Temp <chr>, URL Temp <lgl>, …

    ## Rows: 6
    ## Columns: 27
    ## $ `Unique ID`                                              <dbl> 25747, 25748,…
    ## $ Name                                                     <chr> "Mark A. Hort…
    ## $ Age                                                      <dbl> 21, 19, 17, 2…
    ## $ Gender                                                   <chr> "Male", "Male…
    ## $ Race                                                     <chr> "African-Amer…
    ## $ `URL of image`                                           <chr> NA, NA, NA, N…
    ## $ `Date of injury resulting in death (month/day/year)`     <chr> "1/1/2000", "…
    ## $ `Location of injury (address)`                           <chr> "Davison Free…
    ## $ `Location of death (city)`                               <chr> "Detroit", "D…
    ## $ State                                                    <chr> "MI", "MI", "…
    ## $ `Location of death (zip code)`                           <dbl> 48203, 48203,…
    ## $ `Location of death (county)`                             <chr> "Wayne", "Way…
    ## $ `Full Address`                                           <chr> "Davison Free…
    ## $ Latitude                                                 <dbl> 42.40453, 42.…
    ## $ Longitude                                                <dbl> -83.09227, -8…
    ## $ `Agency or agencies involved`                            <chr> NA, NA, "Mend…
    ## $ `Highest level of force`                                 <chr> "Vehicle", "V…
    ## $ `Alleged weapon`                                         <chr> NA, NA, NA, N…
    ## $ `Aggressive physical movement`                           <chr> NA, NA, NA, N…
    ## $ `Fleeing/Not fleeing`                                    <chr> NA, NA, NA, N…
    ## $ `Description Temp`                                       <chr> NA, NA, NA, N…
    ## $ `URL Temp`                                               <lgl> NA, NA, NA, N…
    ## $ `Brief description`                                      <chr> "Two Detroit …
    ## $ `Dispositions/Exclusions INTERNAL USE, NOT FOR ANALYSIS` <chr> "Unreported",…
    ## $ `Intended use of force (Developing)`                     <chr> "Pursuit", "P…
    ## $ `Supporting document link`                               <chr> "https://driv…
    ## $ `Foreknowledge of mental illness`                        <chr> "No", "No", "…
>>>>>>> 58e0625343d405dad80dc6302365229af6ecd355

## 3. Data analysis plan

Main hypothesis is whether there is a link between dying by the police
and being innocent. Our prediction is there is not a significant link
between the two factors. The variables we will use to answer the
question are: highest level of force, alleged weapon, aggressive
physical movement, fleeing / not fleeing, dispositions / exclusions. A
comparison group could be any of the following or all the following
categories, aggressive physical movement, alleged weapon, fleeing / not
fleeing. Side hypothesis’ could include: whether there is a link between
race and being killed by the police, whether there is a link to age and
being killed by the police, whether there is a link between what state
you are in and being killed by the police, whether there is a link
between mental health and being killed by the police. The percentage of
innocent people who died out of all the people who died, could be a
useful indicator, bar chart with variables fleeing and not fleeing,
graph showing out of the people who died if they had a weapon what
weapon they had, whether an aggressive physical movement increases your
chances of being killed, out of the innocent people who died what were
they killed by may be a difference between being shot and killed in a
police pursuit. Out of the people who we put in our “innocent” group how
many of the cases had dispositions or exclusions.

``` data_visualisation
Innocent_Deaths_caused_by_Police_All_time_ %>% 
  group_by(Age) %>% 
  ggplot(aes(x = Age)) +
  geom_histogram()
```

Data is right skewed, shows the most likely age to die from the police
is between 25 and 35. There also appears to be a data point below the
age of zero which highly unlikely. So in the project we will filter that
out.
