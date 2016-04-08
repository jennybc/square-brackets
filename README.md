square bracket
================

``` r
file.remove(list.files(pattern = "\\.(md|html)$"))
```

    ## [1] TRUE TRUE TRUE TRUE TRUE TRUE

``` r
rmarkdown::render("output-html-keep-md.Rmd", quiet = TRUE)
rmarkdown::render("output-md.Rmd", quiet = TRUE)
system('pandoc output-md.md -o output-md.html')
rmarkdown::render("output-github.Rmd", quiet = TRUE)
system('pandoc output-github.md -o output-github.html')
```
