
<!-- badges: start -->

[![R-CMD-check](https://github.com/caravagnalab/pkgTemplate/workflows/R-CMD-check/badge.svg)](https://github.com/caravagnalab/pkgTemplate/actions)
<!-- badges: end -->

## Template for a R Package repository

Content related to the package:

-   `DESCRIPTION`: contains information about the package
    name/description and dependencies. `Imports` is used to import CRAN
    packages, while dependencies installed from github must be present
    also in the `Remotes` field.

-   `NAMESPACE`: contains all the imported packages and functions.
    Automatically generated by `devtools::document()`, should not be
    modified.

-   `man`: contains the manual reference for the exported functions.
    Automatically generated by `devtools::document()` and files should
    not be modified.

-   `R`: contains all the `R` scripts of the package.

## To create an empty package from RStudio

1.  `File`
2.  `New Project`
3.  `New Directory`
4.  `R Package`
5.  Set the package name and the location on disk

## Other functions

To load the functions without installing the package (from inside the
package directory):

-   `devtools::load_all()`

To document the package with Roxygen (updating `NAMESPACE` and the
manual):

-   `devtools::document()`

To add a dataset to the package:

-   `usethis::use_data(trees)` to add the object `trees` as package
    data.

To build the site locally:

-   `pkgdown::build_site()`

    Calling `build_site()` will generate a folder `docs` with the
    `.html` files of the website built locally. If the GitHub Actions
    workflow to build the website is working (`pkgdown` in this
    repository), the website will be automatically built each time a
    change is pushed, so `docs` should be in the `.gitignore` since it
    is not useful.

To create an article:

-   `usethis::use_article("hello")`

    This will generate a file `hello.Rmd` in the `vignettes` folder.
