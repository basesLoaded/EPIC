
<!-- README.md is generated from README.Rmd. Please edit that file -->
EPIC - package
==============

Description
-----------

Package implementing EPIC method to estimate the proportion of immune and cancer cells from bulk gene expression data. It is based on reference gene expression profiles for the main immune cell types and it predicts the proportion of these cells and of the remaining "other cells" that are the remaining cells (cancer, stromal, endothelial) for which no reference profile is given.

Usage
-----

The main function in this package is `EPIC`. It needs as input a matrix of the raw gene expression counts from the samples for which to estimate cell proportions. One can also define the reference cells to use

``` r
out <- EPIC(bulk = bulkSamplesMatrix)
out <- EPIC(bulk = bulkSamplesMatrix, reference = referenceCellsList)
```

`out` is a list containing the various mRNA and cell fractions in each samples as well as some *data.frame* of the goodness of fit.

Values of mRNA per cell and signature genes to use can also be changed:

``` r
out <- EPIC(bulk = bulkSamplesMatrix, reference = referenceCellsList, mRNA_cell = mRNA_cell_vector, sigGenes = sigGenes_vector)
out <- EPIC(bulk = bulkSamplesMatrix, reference = referenceCellsList, mRNA_cell_sub = mRNA_cell_sub_vector)
```

Installation
------------

``` r
install.packages("devtools")
devtools::install_github("GfellerLab/EPIC")
```
