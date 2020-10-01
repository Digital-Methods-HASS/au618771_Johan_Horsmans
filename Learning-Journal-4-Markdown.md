Learning Journal 4
================
Johan Horsmans (AU618771)

Use R to figure out how many elements in the vector below are greater
than 2 . (You need to filter out the NAs
first)

``` r
rooms <- c(1, 2, 1, 3, 1, NA, 3, 1, 3, 2, 1, NA, 1, 8, 3, 1, 4, NA, 1, 3, 1, 2, 1, 7, 1, NA) #Create the rooms data objet
rooms<-na.omit(rooms) #clean data (i.e. remove NA's)

length(rooms[rooms > 2]) #Index the elements in 'rooms' which are larger than 2 and take the length of these elements.
```

    ## [1] 8

What is the result of running median() function on the above ‘rooms’
vector? (again, best remove the NAs)

``` r
median(rooms)
```

    ## [1] 1.5

Inside your R Project (.Rproj), install the ‘tidyverse’ package and use
the download.file() and read\_csv() function to read the SAFI\_clean.csv
dataset into your R project as ‘interviews’ digital object (see
instructions in <https://datacarpentry.org/r-socialsci/setup.html> and
‘Starting with Data’ section). Take a screenshot of your RStudio
interface showing a) the script you used to create the object, b) the
‘interviews’ object in the Environment and the c) structure of your R
project in the bottom right Files pane. Save the screenshot as an image
and put it in your AUID\_lastname\_firstname repository inside our
Github organisation (github.com/Digital-Methods-HASS). Place here the
URL leading to the screenshot in your
    repository.

``` r
library(tidyverse) #Tidyverse was already installed on my computer.
```

    ## -- Attaching packages ------------------------------------------------------------------------- tidyverse 1.3.0 --

    ## v ggplot2 3.3.2     v purrr   0.3.4
    ## v tibble  3.0.1     v dplyr   1.0.0
    ## v tidyr   1.0.2     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.5.0

    ## Warning: package 'ggplot2' was built under R version 4.0.2

    ## Warning: package 'dplyr' was built under R version 4.0.2

    ## -- Conflicts ---------------------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
download.file("https://ndownloader.figshare.com/files/11492171","data/SAFI_clean.csv",mode="wb") #Download data to the "data" folder in my repository/working directory.

interviews=read.csv("Data/SAFI_clean.csv") #Read the SAFI_clean.csv file and save it as an object named "interviews".
```

Here is the link to my screenshot:
<https://github.com/Digital-Methods-HASS/au618771_Johan_Horsmans/blob/master/Screenshot.JPG>
