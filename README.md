mboxr
=====

[![License: GPL
v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
[![Travis build
status](https://travis-ci.org/jooyoungseo/mboxr.svg?branch=master)](https://travis-ci.org/jooyoungseo/mboxr)
[![AppVeyor build
status](https://ci.appveyor.com/api/projects/status/github/jooyoungseo/mboxr?branch=master&svg=true)](https://ci.appveyor.com/project/jooyoungseo/mboxr)
[![Codecov test
coverage](https://codecov.io/gh/jooyoungseo/mboxr/branch/master/graph/badge.svg)](https://codecov.io/gh/jooyoungseo/mboxr?branch=master)

The goal of mboxr is to allow R users to conveniently import an mbox
file into R tibble for hands-on analyses in R environment.

Installation
============

Python Dependencies
-------------------

`mboxr` requires Anaconda Python environment on your system Path.

If you have not installed Conda environment on your system, please
[download and install Anaconda](https://www.anaconda.com/download/)
(Python 3.6 or later is recommended).

R Package Installation
----------------------

### Development Version

You can install the latest development version as follows:

``` r
if(!require(devtools)) {
install.packages("devtools")
}

devtools::install_github("jooyoungseo/mboxr")
```

### Stable Version

You can install the released version of mboxr from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages('mboxr')
```

Usage
-----

Please use `read_mbox()` function after loading `mboxr` library like
below:

``` r
library(mboxr)
# Importing your mbox file into an R:
data <- read_mbox("your_file.mbox")

# Or, you can save your mbox file as a CSV file while assigning a tibble variable at the same time like below :
data <- read_mbox("your_file.mbox", "output.csv")

# You can merge all mbox files in your current directory into one tibble and save csv file for the integrated one:
all_data <- merge_mbox_all(out = "all_merged_mbox.csv")
## Find your "output.csv" file saved in your computer while freely using the imported tibble in your R session!
```
