# moviesApp

`moviesApp` provides the code examples for [Shiny App-Packages](https://mjfrigaard.github.io/shinyap/).

## Code for book

You can view the GitHub repository for the book [here](https://github.com/mjfrigaard/shinyap).

## `movies` app

The original code and data for this shiny app comes from the [Building Web Applications with Shiny](https://rstudio-education.github.io/shiny-course/) course.

I've converted it have [shiny modules](https://shiny.posit.co/r/articles/improve/modules/) and a [standalone app function](https://mastering-shiny.org/scaling-packaging.html#converting-an-existing-app) (which can be run from `app.R`).

# Branches

View the various versions of application in the [`moviesApp` branches](https://github.com/mjfrigaard/moviesApp/branches/all).

## Tests 

### `12e_tests-modules`

[`12e_tests-modules`](https://github.com/mjfrigaard/moviesApp/tree/12e_tests-modules) gives examples of Shiny's `testServer()` function.

```
tests
├── testthat
│   ├── _snaps
│   │   └── scatter_plot
│   │       ├── fr3-color-coded-data-points.svg
│   │       └── fr4-plot-axis-legend-title.svg
│   ├── fixtures
│   │   ├── make_tidy_ggp2_movies.R
│   │   └── tidy_ggp2_movies.rds
│   ├── helper.R
│   ├── test-mod_scatter_display.R
│   ├── test-mod_var_input.R
│   └── test-scatter_plot.R
└── testthat.R

5 directories, 9 files
```



### `12d_tests-mocks`

[`12d_tests-mocks`](https://github.com/mjfrigaard/moviesApp/tree/12d_tests-mocks) demonstrates simulating behaviors with test 'mocks.'

```
tests
├── testthat
│   ├── _snaps
│   │   └── scatter_plot
│   │       ├── fr12-fr14-initial-x-y-z-axes.svg
│   │       └── fr14-fr15-update-x-y-color.svg
│   ├── fixtures
│   │   ├── make_tidy_ggp2_movies.R
│   │   └── tidy_ggp2_movies.rds
│   ├── helper.R
│   └── test-scatter_plot.R
└── testthat.R

5 directories, 7 files
```


### `12c_tests-helpers`

[`12c_tests-helpers`](https://github.com/mjfrigaard/moviesApp/tree/12c_tests-helpers) explores using test helpers with unit tests.

```
tests
├── testthat
│   ├── fixtures
│   │   ├── make_tidy_ggp2_movies.R
│   │   └── tidy_ggp2_movies.rds
│   ├── helper.R
│   └── test-scatter_plot.R
└── testthat.R
3 directories, 5 files
```

### `12b_tests-fixtures`

[`12b_tests-fixtures`](https://github.com/mjfrigaard/moviesApp/tree/12b_tests-fixtures) explores adding `tests/testthat/fixtures/` for static data: 

```
tests
├── testthat
│   ├── fixtures
│   │   ├── make_tidy_ggp2_movies.R
│   │   └── tidy_ggp2_movies.rds
│   └── test-scatter_plot.R
└── testthat.R

3 directories, 4 files
```

### `12a_tests-specs`

[`12a_tests-specs`](https://github.com/mjfrigaard/moviesApp/tree/12a_tests-specs) covers working through a set of app specifications and building a traceability matrix. 

`usethis::use_testthat(3)` adds the following to the `DESCRIPTION`:

```
Config/testthat/edition: 3
```

Creating a new test file with `usethis::use_test("scatter_plot")`

```
tests
├── testthat
│   └── test-scatter_plot.R
└── testthat.R

2 directories, 2 files
```

`usethis::use_vignette('test-specs')` adds the following to the `DESCRIPTION`:

```
VignetteBuilder: knitr
```

```
vignettes/
└── test-specs.Rmd

1 directory, 1 file
```

## External resources 

### `11d_inst-prod`

[`11d_inst-prod`](https://github.com/mjfrigaard/moviesApp/tree/11d_inst-prod) gives an example of storing a 'production' version of your application in the `inst/prod/` folder.

```
inst
├── dev
│   ├── app.R
│   ├── imdb.png
│   └── tidy_movies.fst
├── extdata
│   └── movies.fst
├── prod
│   └── app
│       └── app.R
└── www
    ├── bootstrap.png
    └── shiny.png

6 directories, 7 files
```

### `11c_inst-dev`

[`11c_inst-dev`](https://github.com/mjfrigaard/moviesApp/tree/11c_inst-dev) stores a development version of the primary application in `inst/dev/`.

```
inst
├── dev
│   ├── app.R
│   ├── imdb.png
│   └── tidy_movies.fst
├── extdata
│   └── movies.fst
└── www
    ├── bootstrap.png
    └── shiny.png

4 directories, 6 files
```

### `11b_inst-bslib`

[`11b_inst-bslib`](https://github.com/mjfrigaard/moviesApp/tree/11b_inst-bslib) covers how to store external files use the application UI function to display alternative versions of your app.

```
inst
├── extdata
│   └── movies.fst
└── www
    ├── bootstrap.png
    └── shiny.png

3 directories, 3 files
```

### `11a_inst-www`

[`11a_inst-www`](https://github.com/mjfrigaard/moviesApp/tree/11a_inst-www) shows how to add external resources in your app-package (i.e., the files previously stored in `www/`).

```
inst
├── extdata
│   └── movies.fst
└── www
    └── shiny.png

3 directories, 2 files
```

## `10_launch-app`

[`10_launch-app`](https://github.com/mjfrigaard/moviesApp/tree/10_launch-app) gives advice on what to put in the `app.R` file, and which function to use for launching vs. deploying the application.

## `09_data`

[`09_data`](https://github.com/mjfrigaard/moviesApp/tree/09_data) covers the various ways to store data in your app-package.

Data for the package (internal, becomes part of the namespace)

```
data
├── movies.RData
└── movies.rda

1 directory, 2 files
```

External data files

```
inst
└── extdata
    └── movies.fst

2 directories, 1 file
```


## Dependencies

The following branches (`08a_pkg-exports` and `08b_pkg-imports`) cover imports and exports:


### `08b_pkg-imports`

The [`08b_pkg-imports`](https://github.com/mjfrigaard/moviesApp/tree/08b_pkg-imports) branch of `moviesApp` covers how to import functions from add-on packages so we can use them in our package.

Changes in the `DESCRIPTION` 

```
Package: moviesApp
Title: movies app
Version: 0.0.0.9000
Author: John Smith <John.Smith@email.io> [aut, cre]
Maintainer: John Smith <John.Smith@email.io>
Description: A movie-review shiny application.
License: GPL-3
Encoding: UTF-8
Roxygen: list(markdown = TRUE)
RoxygenNote: 7.2.3
Imports: 
    ggplot2,
    rlang,
    shiny,
    shinythemes,
    stringr
```

Changes in the `NAMESPACE`

```
# Generated by roxygen2: do not edit by hand

export(movies_app)
export(scatter_plot)
import(shiny)
importFrom(rlang,.data)
```



### `08a_pkg-exports`

The [`08a_pkg-exports`](https://github.com/mjfrigaard/moviesApp/tree/08a_pkg-exports) branch of `moviesApp` covers how to export functions from our package for users in the `NAMESPACE`

```
# Generated by roxygen2: do not edit by hand

export(movies_app)
export(scatter_plot)
```


## `07_roxygen2`

The [`07_roxygen2`](https://github.com/mjfrigaard/moviesApp/tree/07_roxygen2) branch of `moviesApp` has documentation for all files in `R/`, and creates the help files in the `man/` folder:

```
man
├── mod_scatter_display_server.Rd
├── mod_scatter_display_ui.Rd
├── mod_var_input_server.Rd
├── mod_var_input_ui.Rd
├── movies_app.Rd
├── movies_server.Rd
├── movies_ui.Rd
└── scatter_plot.Rd

1 directory, 8 files
```

## Creating packages

The next two branches cover creating packages with `usethis::create_package()` and by manually editing the `DESCRIPTION` file.

### `06b_devtools`

Manually converting the package with the `DESCRIPTION` doesn't include `Roxygen: list(markdown = TRUE)` (but it's covered in the following branches)

```
Package: moviesApp
Title: movies app
Version: 0.0.0.9000
Author: John Smith [aut, cre]
Maintainer: John Smith <John.Smith@email.io>
Description: A movie-review shiny application.
License: GPL-3
RoxygenNote: 7.2.3
Encoding: UTF-8
```

### `06a_create-package`

After running `usethis::create_package()`, the `DESCRIPTION` file is updated with the following fields:

```
Package: moviesApp
Title: movies app
Version: 0.0.0.9000
Author: John Smith [aut, cre]
Maintainer: John Smith <John.Smith@email.io>
Description: A movie-review shiny application.
License: GPL-3
Encoding: UTF-8
Roxygen: list(markdown = TRUE)
RoxygenNote: 7.2.3
```


## `05_rproj`

The `moviesApp.Rproj` file now contains the following fields: 

```
Version: 1.0

RestoreWorkspace: Default
SaveWorkspace: Default
AlwaysSaveHistory: Default

EnableCodeIndexing: Yes
UseSpacesForTab: Yes
NumSpacesForTab: 2
Encoding: UTF-8

RnwWeave: Sweave
LaTeX: XeLaTeX

BuildType: Package
PackageUseDevtools: Yes
PackageInstallArgs: --no-multiarch --with-keep.source
PackageRoxygenize: rd,collate,namespace
```

## `04_description`

The [`04_description`](https://github.com/mjfrigaard/moviesApp/tree/04_description) branch of `moviesApp` has an updated `DESCRIPTION` file:

```
Package: moviesApp
Title: movies app
Version: 0.0.0.9000
Author: John Smith [aut, cre]
Maintainer: John Smith <John.Smith@email.io>
Description: A movie-review shiny application.
License: GPL-3
```

## `03_proj-app`

The [`03_proj-app`](https://github.com/mjfrigaard/moviesApp/tree/03_proj-app) branch of `moviesApp` includes and `R/` folder and external resources have been included in `www`. 

```
R/
├── mod_scatter_display.R
├── mod_var_input.R
└── utils.R

1 directory, 3 files
```

```
www/
└── shiny.png

1 directory, 1 file
```


A `DESCRIPTION` file has also been added.

```
Type: shiny
Title: movies app
Author: John Smith
DisplayMode: Showcase
```

## `02_movies-app`

The [`02_movies-app`](https://github.com/mjfrigaard/moviesApp/tree/02_movies-app) branch of `moviesApp` includes the code for the movie review data (from the [Building Web Applications with Shiny](https://rstudio-education.github.io/shiny-course/) course) in `app.R`.

## `main`

The [`main`](https://github.com/mjfrigaard/moviesApp/tree/main) branch of `moviesApp` is identical to the files that are created with a new Shiny App from the Posit Workbench New Project Wizard.
