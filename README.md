
<!-- README.md is generated from README.Rmd. Please edit that file -->
shed
====

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

![shed](inst/img/shed.png)

A minimal, eye-friendly csv editor made with [shiny](https://CRAN.R-project.org/package=shiny), [rhandsontable](https://CRAN.R-project.org/package=rhandsontable), and [readr](https://CRAN.R-project.org/package=readr). Shed is designed to quickly edit small (hundreds of rows) csv files and `data.frames` and save them as UTF-8 encoded csv files.

Why use shed?
-------------

Use shed if you need to manually edit csv files in a GUI, but you cannot or do not want to install a dedicated csv-editor (for example, on a remote RStudio server). Shed is arguably more confortable and safe to use than Excel which is notorious for converting everything that looks remotely like a date to strangely formatted dates. It cannot compete with dedicated csv editors in terms of performance and can only handle csv files with a few hundred to a thousand rows before it becomes noticably slugish.

Development status
------------------

**shed is currently beeing rewritten. A finished CRAN ready version is planned for mid 2019 as I wanna finish some other projects first**

shed is perfectly usable and the internals are more or less stable. The user interface might still change a bit, especially how files are read and written. There is also an [issue in rhandsontable](https://github.com/jrowen/rhandsontable/issues/264) which I want to see fixed - or figure out a workaround for - before I plan on putting shed on CRAN.

If you have any feature requests or comments don't hesitate to file an issue or send a mail.

Installation
------------

You can install shed from github with:

``` r
# install.packages("devtools")
devtools::install_github("s-fleck/shed")
```

Example
-------

``` r
shed(iris)

# Uppon termination, shed returns the edited data.frame

x <- shed(iris)
```
