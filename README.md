# Official documentation of the CellexalVR backend R package

The documentation is build using R::bookdown.

```
bookdown::render_book('.', "bookdown::gitbook", output_dir = "_book" )
```

In order to build this 'book' you need a set of R packages installed:

```
lapply( c('bookdown', 'umap', "BiocManager", "devtools", 'Seurat' ), function(package) {
    if (!require( package, quietly = TRUE))
        install.packages( c( package ) )
})

lapply( c('flowCore' ), function(package) {
    if (!require( package, quietly = TRUE))
        BiocManager::install( c( package ) )
})


if (!require( 'cellexalvrR', quietly = TRUE))
    devtools::install_github( "sonejilab/cellexalvrR" )

```