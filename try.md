BA\&A - R-Markdown, introduction
================
mcordobaa
12/03/2021

#### tamaño mediano

# tamaño

##### based on <https://ourcodingclub.github.io/tutorials/rmarkdown/>

### R Markdown

R Markdown allows you to create documents that serve as a neat record of
your analysis. In the world of reproducible research, we want other
researchers to easily understand what we did in our analysis, otherwise
nobody can be certain that you analysed your data properly. You might
choose to create an RMarkdown document as an appendix to a paper or
project assignment that you are doing, upload it to an online repository
such as Github, or simply to keep as a personal record so you can
quickly look back at your code and see what you did. RMarkdown presents
your code alongside its output (graphs, tables, etc.) with conventional
text to explain it, a bit like a notebook.

### syntax

RMarkdown uses Markdown syntax. Markdown is a very simple ‘markup’
language which provides methods for creating documents with headers,
images, links etc. from plain text files, while keeping the original
plain text file easy to read. You can convert Markdown documents to many
other file types like .html or .pdf to display the headers, images etc..

#### Basic syntax

· Font size is manipulated with “\#” :

# header

## header

### header

#### header

· *italica*

· **Negrita**

#### Insert links:

[Google](https://www.google.com)

## Including plots and code

``` r
# library
library(ggplot2)
```

    ## Warning: package 'ggplot2' was built under R version 4.0.2

``` r
# dataset:
data=data.frame(value=rnorm(100))

# basic histogram
p <- ggplot(data, aes(x=value)) + 
  geom_histogram()

p
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](try_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

## Including only Plots, without messages, erros or codes

![](try_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

##### make tables

``` r
x= c(1,2,3)
y= c(4,5,6)
z=c(7,8,9)
table= cbind(x,y,z)
as.table(table)
```

    ##   x y z
    ## A 1 4 7
    ## B 2 5 8
    ## C 3 6 9

#### You can include chunks with other programming languages, e.g. bash

``` bash
less -S ./Tesis/Datos_Aguacate/outputs/table_11k_LE.tsv |  head
```

    ## OTU ID   A1  A10 A11 A12 A13 A14 A15 A16 A2  A3  A4  A5  A6  A7  A8  A9
    ## 8467f0ab0e259de42b817d54b8485553 22.0    30.0    37.0    48.0    26.0    16.0    14.0    46.0    18.0    38.0    28.0    50.0    28.0    14.0    17.0    34.0
    ## 31aa3015f6fe768d7e2d1fdf2883d1a3 28.0    29.0    20.0    25.0    27.0    28.0    14.0    18.0    25.0    24.0    19.0    44.0    17.0    16.0    43.0    49.0
    ## 1f5e4e565e9e50e85cd6bbc4e512af42 19.0    17.0    19.0    41.0    26.0    22.0    18.0    46.0    19.0    19.0    21.0    39.0    24.0    22.0    17.0    32.0
    ## 5c9aab1dba9b82d25584168eff10bb29 26.0    25.0    12.0    27.0    28.0    28.0    22.0    9.0 27.0    23.0    16.0    25.0    21.0    27.0    32.0    40.0
    ## d58a4c78198ff88d9398a519e2e4cdb3 12.0    29.0    14.0    16.0    19.0    27.0    31.0    61.0    66.0    18.0    44.0    35.0    21.0    26.0    21.0    32.0
    ## 2f1540f26a6934e80d568a4b6bce7fbd 12.0    9.0 9.0 0.0 23.0    49.0    54.0    36.0    30.0    0.0 18.0    11.0    0.0 6.0 247.0   14.0
    ## fe40c67afa7a434a2514cc87677a274c 13.0    36.0    26.0    16.0    18.0    16.0    16.0    0.0 0.0 10.0    0.0 25.0    26.0    19.0    21.0    21.0
    ## 95703a5778f4d3d5cc5b01137883bfcd 14.0    31.0    17.0    22.0    12.0    26.0    25.0    0.0 50.0    20.0    37.0    24.0    19.0    26.0    14.0    23.0
    ## b9a98170de4a567e45f613ae259c7797 16.0    6.0 10.0    0.0 21.0    0.0 69.0    25.0    35.0    0.0 32.0    8.0 0.0 9.0 227.0   7.0

Tutorials:

<https://guides.github.com/features/mastering-markdown/>

<https://ourcodingclub.github.io/tutorials/rmarkdown/>

<https://rmarkdown.rstudio.com/lesson-15.html>

<https://rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf?_ga=2.114854916.2005358188.1614346276-1239002712.1614346276>
