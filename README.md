<!-- README.md is generated from README.Rmd. Please edit that file -->

Wes Anderson Palettes (modified)
================================

Installation
------------

``` r
devtools::install_github("devanmcg/wesanderson")
```

Usage
-----

``` r
library("wesanderson")
```

``` r
# See all palettes
names(wes_palettes)
#>  [1] "BottleRocket1"  "BottleRocket2"  "Rushmore1"      "Rushmore"      
#>  [5] "Royal1"         "Royal2"         "Zissou1"        "Darjeeling1"   
#>  [9] "Darjeeling2"    "Chevalier1"     "FantasticFox1"  "Moonrise1"     
#> [13] "Moonrise2"      "Moonrise3"      "Cavalcanti1"    "GrandBudapest1"
#> [17] "GrandBudapest2" "IsleofDogs1"    "IsleofDogs2"    "DeadLiveStrong"
#> [21] "DeadLiveLight"  "FuelMoisture4"  "FuelMoisture5"
```

Palettes
--------

### Bottle Rocket (1996)

``` r
wes_palette("BottleRocket1")
```

![](figure/bottlerocket1-1.png)

``` r
wes_palette("BottleRocket2")
```

![](figure/bottlerocket1-2.png)

### Rushmore (1998)

``` r
wes_palette("Rushmore1")
```

![](figure/rushmore-1.png)

### The Royal Tenenbaums (2001)

``` r
wes_palette("Royal1")
```

![](figure/royal-1.png)

``` r
wes_palette("Royal2")
```

![](figure/royal-2.png)

``` r
library("ggplot2")
#> Warning: package 'ggplot2' was built under R version 4.0.4
ggplot(mtcars, aes(factor(cyl), fill=factor(vs))) +  geom_bar() +
  scale_fill_manual(values = wes_palette("Royal1"))
```

![](figure/ggplot1-1.png)

### The Life Aquatic with Steve Zissou (2004)

``` r
wes_palette("Zissou1")
```

![](figure/lifeaquatic-1.png)

``` r
pal <- wes_palette("Zissou1", 21, type = "continuous")
image(volcano, col = pal)
```

![](figure/volcano-1.png)

``` r
pal <- wes_palette("Zissou1", 100, type = "continuous")
# heatmap is a local dataset
ggplot(heatmap, aes(x = X2, y = X1, fill = value)) +
  geom_tile() + 
  scale_fill_gradientn(colours = pal) + 
  scale_x_discrete(expand = c(0, 0)) +
  scale_y_discrete(expand = c(0, 0)) + 
  coord_equal() 
```

![](figure/zissou_heatmap-1.png)

### The Darjeeling Limited (2007)

``` r
wes_palette("Darjeeling1")
```

![](figure/darjeeling-1.png)

``` r
wes_palette("Darjeeling2")
```

![](figure/darjeeling-2.png)

### Hotel Chevalier (2007)

``` r
wes_palette("Chevalier1")
```

![](figure/chevalier-1.png)

### Fantastic Mr. Fox (2009)

``` r
wes_palette("FantasticFox1")
```

![](figure/fantasticfox-1.png)

### Moonrise Kingdom (2012)

``` r
wes_palette("Moonrise1")
```

![](figure/moonrise-1.png)

``` r
wes_palette("Moonrise2")
```

![](figure/moonrise-2.png)

``` r
wes_palette("Moonrise3")
```

![](figure/moonrise-3.png)

### Castello Cavalcanti (2013)

``` r
wes_palette("Cavalcanti1")
```

![](figure/castello-1.png)

### The Grand Budapest Hotel (2014)

``` r
wes_palette("GrandBudapest1")
```

![](figure/grandbudapest-1.png)

``` r
wes_palette("GrandBudapest2")
```

![](figure/grandbudapest-2.png)

### The Isle of Dogs (2018)

``` r
wes_palette("IsleofDogs1")
```

![](figure/isleofdogs-1.png)

``` r
wes_palette("IsleofDogs2")
```

![](figure/isleofdogs-2.png)
