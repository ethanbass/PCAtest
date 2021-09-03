
<!-- README.md is generated from README.Rmd. Please edit that file -->

# PCAtest

<!-- badges: start -->

<!-- badges: end -->

The goal of PCAtest is to evaluate the overall significance of a PCA, of
each PC axis, and of the contributions of each observed variable to the
significant axes based on permutation-based statistical tests. PCAtest
uses random permutations to build null distributions for several
statistics of a PCAanalysis: Psi (Vieira 2012), Phi (Gleason and Staelin
1975), the rank-of-roots (ter Braak 1988), the index of the loadings
(Vieira 2012), and the correlations of the PC with the variables
(Jackson 1991). Comparing these distributions with the observed values
of the statistics, the function tests: (1) the hypothesis that there is
more correlational structure among the observed variables than expected
by random chance, (2) the statistical significance of each PC, and (3)
the contribution of each observed variable to each significant PC. The
function also calculates the sampling variance around mean observed
statistics based on bootstrap replicates.

## Installation

You can install the released and the development versions from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("arleyc/PCAtest")
```

## Example

``` r
library(PCAtest)
# PCA analysis of two uncorrelated variables
v1<-runif(100,0,1)
v2<-runif(100,0,1)
x<-cbind(v1,v2)
result<-PCAtest(x, 100, 100, 0.05, corr=FALSE, plot=TRUE)
#>  1 of 100 bootstrap replicates 2 of 100 bootstrap replicates 3 of 100 bootstrap replicates 4 of 100 bootstrap replicates 5 of 100 bootstrap replicates 6 of 100 bootstrap replicates 7 of 100 bootstrap replicates 8 of 100 bootstrap replicates 9 of 100 bootstrap replicates 10 of 100 bootstrap replicates 11 of 100 bootstrap replicates 12 of 100 bootstrap replicates 13 of 100 bootstrap replicates 14 of 100 bootstrap replicates 15 of 100 bootstrap replicates 16 of 100 bootstrap replicates 17 of 100 bootstrap replicates 18 of 100 bootstrap replicates 19 of 100 bootstrap replicates 20 of 100 bootstrap replicates 21 of 100 bootstrap replicates 22 of 100 bootstrap replicates 23 of 100 bootstrap replicates 24 of 100 bootstrap replicates 25 of 100 bootstrap replicates 26 of 100 bootstrap replicates 27 of 100 bootstrap replicates 28 of 100 bootstrap replicates 29 of 100 bootstrap replicates 30 of 100 bootstrap replicates 31 of 100 bootstrap replicates 32 of 100 bootstrap replicates 33 of 100 bootstrap replicates 34 of 100 bootstrap replicates 35 of 100 bootstrap replicates 36 of 100 bootstrap replicates 37 of 100 bootstrap replicates 38 of 100 bootstrap replicates 39 of 100 bootstrap replicates 40 of 100 bootstrap replicates 41 of 100 bootstrap replicates 42 of 100 bootstrap replicates 43 of 100 bootstrap replicates 44 of 100 bootstrap replicates 45 of 100 bootstrap replicates 46 of 100 bootstrap replicates 47 of 100 bootstrap replicates 48 of 100 bootstrap replicates 49 of 100 bootstrap replicates 50 of 100 bootstrap replicates 51 of 100 bootstrap replicates 52 of 100 bootstrap replicates 53 of 100 bootstrap replicates 54 of 100 bootstrap replicates 55 of 100 bootstrap replicates 56 of 100 bootstrap replicates 57 of 100 bootstrap replicates 58 of 100 bootstrap replicates 59 of 100 bootstrap replicates 60 of 100 bootstrap replicates 61 of 100 bootstrap replicates 62 of 100 bootstrap replicates 63 of 100 bootstrap replicates 64 of 100 bootstrap replicates 65 of 100 bootstrap replicates 66 of 100 bootstrap replicates 67 of 100 bootstrap replicates 68 of 100 bootstrap replicates 69 of 100 bootstrap replicates 70 of 100 bootstrap replicates 71 of 100 bootstrap replicates 72 of 100 bootstrap replicates 73 of 100 bootstrap replicates 74 of 100 bootstrap replicates 75 of 100 bootstrap replicates 76 of 100 bootstrap replicates 77 of 100 bootstrap replicates 78 of 100 bootstrap replicates 79 of 100 bootstrap replicates 80 of 100 bootstrap replicates 81 of 100 bootstrap replicates 82 of 100 bootstrap replicates 83 of 100 bootstrap replicates 84 of 100 bootstrap replicates 85 of 100 bootstrap replicates 86 of 100 bootstrap replicates 87 of 100 bootstrap replicates 88 of 100 bootstrap replicates 89 of 100 bootstrap replicates 90 of 100 bootstrap replicates 91 of 100 bootstrap replicates 92 of 100 bootstrap replicates 93 of 100 bootstrap replicates 94 of 100 bootstrap replicates 95 of 100 bootstrap replicates 96 of 100 bootstrap replicates 97 of 100 bootstrap replicates 98 of 100 bootstrap replicates 99 of 100 bootstrap replicates 100 of 100 bootstrap replicatesCalculating confidence intervals of empirical statistics... Please wait 1 of 100 random permutations                                                  2 of 100 random permutations                                                  3 of 100 random permutations                                                  4 of 100 random permutations                                                  5 of 100 random permutations                                                  6 of 100 random permutations                                                  7 of 100 random permutations                                                  8 of 100 random permutations                                                  9 of 100 random permutations                                                  10 of 100 random permutations                                                  11 of 100 random permutations                                                  12 of 100 random permutations                                                  13 of 100 random permutations                                                  14 of 100 random permutations                                                  15 of 100 random permutations                                                  16 of 100 random permutations                                                  17 of 100 random permutations                                                  18 of 100 random permutations                                                  19 of 100 random permutations                                                  20 of 100 random permutations                                                  21 of 100 random permutations                                                  22 of 100 random permutations                                                  23 of 100 random permutations                                                  24 of 100 random permutations                                                  25 of 100 random permutations                                                  26 of 100 random permutations                                                  27 of 100 random permutations                                                  28 of 100 random permutations                                                  29 of 100 random permutations                                                  30 of 100 random permutations                                                  31 of 100 random permutations                                                  32 of 100 random permutations                                                  33 of 100 random permutations                                                  34 of 100 random permutations                                                  35 of 100 random permutations                                                  36 of 100 random permutations                                                  37 of 100 random permutations                                                  38 of 100 random permutations                                                  39 of 100 random permutations                                                  40 of 100 random permutations                                                  41 of 100 random permutations                                                  42 of 100 random permutations                                                  43 of 100 random permutations                                                  44 of 100 random permutations                                                  45 of 100 random permutations                                                  46 of 100 random permutations                                                  47 of 100 random permutations                                                  48 of 100 random permutations                                                  49 of 100 random permutations                                                  50 of 100 random permutations                                                  51 of 100 random permutations                                                  52 of 100 random permutations                                                  53 of 100 random permutations                                                  54 of 100 random permutations                                                  55 of 100 random permutations                                                  56 of 100 random permutations                                                  57 of 100 random permutations                                                  58 of 100 random permutations                                                  59 of 100 random permutations                                                  60 of 100 random permutations                                                  61 of 100 random permutations                                                  62 of 100 random permutations                                                  63 of 100 random permutations                                                  64 of 100 random permutations                                                  65 of 100 random permutations                                                  66 of 100 random permutations                                                  67 of 100 random permutations                                                  68 of 100 random permutations                                                  69 of 100 random permutations                                                  70 of 100 random permutations                                                  71 of 100 random permutations                                                  72 of 100 random permutations                                                  73 of 100 random permutations                                                  74 of 100 random permutations                                                  75 of 100 random permutations                                                  76 of 100 random permutations                                                  77 of 100 random permutations                                                  78 of 100 random permutations                                                  79 of 100 random permutations                                                  80 of 100 random permutations                                                  81 of 100 random permutations                                                  82 of 100 random permutations                                                  83 of 100 random permutations                                                  84 of 100 random permutations                                                  85 of 100 random permutations                                                  86 of 100 random permutations                                                  87 of 100 random permutations                                                  88 of 100 random permutations                                                  89 of 100 random permutations                                                  90 of 100 random permutations                                                  91 of 100 random permutations                                                  92 of 100 random permutations                                                  93 of 100 random permutations                                                  94 of 100 random permutations                                                  95 of 100 random permutations                                                  96 of 100 random permutations                                                  97 of 100 random permutations                                                  98 of 100 random permutations                                                  99 of 100 random permutations                                                  100 of 100 random permutations                                                 Comparing empirical statistics with their null distributions... Please wait
#> ========================================================
#> Test of PCA significance: 2 variables, 100 observations
#> 100 bootstrap replicates, 100 random permutations
#> ========================================================
#> 
#> Empirical Psi = 0.0028, Max null Psi = 0.1748, Min null Psi = 0.0000, p-value = 0.7
#> Empirical Phi = 0.0372, Max null Phi = 0.2956, Min null Phi = 9e-04, p-value = 0.7
#> 
#> PCA is not significant!
```

<img src="man/figures/README-example1-1.png" width="100%" />

``` r
#PCA analysis of two fully-correlated variables
v1<-seq(0,1,0.01)
v2<-seq(0,1,0.01)
x<-cbind(v1,v2)
PCAout<-PCAtest(x, 100, 100, 0.05, corr=FALSE, plot=TRUE)
#>  1 of 100 bootstrap replicates 2 of 100 bootstrap replicates 3 of 100 bootstrap replicates 4 of 100 bootstrap replicates 5 of 100 bootstrap replicates 6 of 100 bootstrap replicates 7 of 100 bootstrap replicates 8 of 100 bootstrap replicates 9 of 100 bootstrap replicates 10 of 100 bootstrap replicates 11 of 100 bootstrap replicates 12 of 100 bootstrap replicates 13 of 100 bootstrap replicates 14 of 100 bootstrap replicates 15 of 100 bootstrap replicates 16 of 100 bootstrap replicates 17 of 100 bootstrap replicates 18 of 100 bootstrap replicates 19 of 100 bootstrap replicates 20 of 100 bootstrap replicates 21 of 100 bootstrap replicates 22 of 100 bootstrap replicates 23 of 100 bootstrap replicates 24 of 100 bootstrap replicates 25 of 100 bootstrap replicates 26 of 100 bootstrap replicates 27 of 100 bootstrap replicates 28 of 100 bootstrap replicates 29 of 100 bootstrap replicates 30 of 100 bootstrap replicates 31 of 100 bootstrap replicates 32 of 100 bootstrap replicates 33 of 100 bootstrap replicates 34 of 100 bootstrap replicates 35 of 100 bootstrap replicates 36 of 100 bootstrap replicates 37 of 100 bootstrap replicates 38 of 100 bootstrap replicates 39 of 100 bootstrap replicates 40 of 100 bootstrap replicates 41 of 100 bootstrap replicates 42 of 100 bootstrap replicates 43 of 100 bootstrap replicates 44 of 100 bootstrap replicates 45 of 100 bootstrap replicates 46 of 100 bootstrap replicates 47 of 100 bootstrap replicates 48 of 100 bootstrap replicates 49 of 100 bootstrap replicates 50 of 100 bootstrap replicates 51 of 100 bootstrap replicates 52 of 100 bootstrap replicates 53 of 100 bootstrap replicates 54 of 100 bootstrap replicates 55 of 100 bootstrap replicates 56 of 100 bootstrap replicates 57 of 100 bootstrap replicates 58 of 100 bootstrap replicates 59 of 100 bootstrap replicates 60 of 100 bootstrap replicates 61 of 100 bootstrap replicates 62 of 100 bootstrap replicates 63 of 100 bootstrap replicates 64 of 100 bootstrap replicates 65 of 100 bootstrap replicates 66 of 100 bootstrap replicates 67 of 100 bootstrap replicates 68 of 100 bootstrap replicates 69 of 100 bootstrap replicates 70 of 100 bootstrap replicates 71 of 100 bootstrap replicates 72 of 100 bootstrap replicates 73 of 100 bootstrap replicates 74 of 100 bootstrap replicates 75 of 100 bootstrap replicates 76 of 100 bootstrap replicates 77 of 100 bootstrap replicates 78 of 100 bootstrap replicates 79 of 100 bootstrap replicates 80 of 100 bootstrap replicates 81 of 100 bootstrap replicates 82 of 100 bootstrap replicates 83 of 100 bootstrap replicates 84 of 100 bootstrap replicates 85 of 100 bootstrap replicates 86 of 100 bootstrap replicates 87 of 100 bootstrap replicates 88 of 100 bootstrap replicates 89 of 100 bootstrap replicates 90 of 100 bootstrap replicates 91 of 100 bootstrap replicates 92 of 100 bootstrap replicates 93 of 100 bootstrap replicates 94 of 100 bootstrap replicates 95 of 100 bootstrap replicates 96 of 100 bootstrap replicates 97 of 100 bootstrap replicates 98 of 100 bootstrap replicates 99 of 100 bootstrap replicates 100 of 100 bootstrap replicatesCalculating confidence intervals of empirical statistics... Please wait 1 of 100 random permutations                                                  2 of 100 random permutations                                                  3 of 100 random permutations                                                  4 of 100 random permutations                                                  5 of 100 random permutations                                                  6 of 100 random permutations                                                  7 of 100 random permutations                                                  8 of 100 random permutations                                                  9 of 100 random permutations                                                  10 of 100 random permutations                                                  11 of 100 random permutations                                                  12 of 100 random permutations                                                  13 of 100 random permutations                                                  14 of 100 random permutations                                                  15 of 100 random permutations                                                  16 of 100 random permutations                                                  17 of 100 random permutations                                                  18 of 100 random permutations                                                  19 of 100 random permutations                                                  20 of 100 random permutations                                                  21 of 100 random permutations                                                  22 of 100 random permutations                                                  23 of 100 random permutations                                                  24 of 100 random permutations                                                  25 of 100 random permutations                                                  26 of 100 random permutations                                                  27 of 100 random permutations                                                  28 of 100 random permutations                                                  29 of 100 random permutations                                                  30 of 100 random permutations                                                  31 of 100 random permutations                                                  32 of 100 random permutations                                                  33 of 100 random permutations                                                  34 of 100 random permutations                                                  35 of 100 random permutations                                                  36 of 100 random permutations                                                  37 of 100 random permutations                                                  38 of 100 random permutations                                                  39 of 100 random permutations                                                  40 of 100 random permutations                                                  41 of 100 random permutations                                                  42 of 100 random permutations                                                  43 of 100 random permutations                                                  44 of 100 random permutations                                                  45 of 100 random permutations                                                  46 of 100 random permutations                                                  47 of 100 random permutations                                                  48 of 100 random permutations                                                  49 of 100 random permutations                                                  50 of 100 random permutations                                                  51 of 100 random permutations                                                  52 of 100 random permutations                                                  53 of 100 random permutations                                                  54 of 100 random permutations                                                  55 of 100 random permutations                                                  56 of 100 random permutations                                                  57 of 100 random permutations                                                  58 of 100 random permutations                                                  59 of 100 random permutations                                                  60 of 100 random permutations                                                  61 of 100 random permutations                                                  62 of 100 random permutations                                                  63 of 100 random permutations                                                  64 of 100 random permutations                                                  65 of 100 random permutations                                                  66 of 100 random permutations                                                  67 of 100 random permutations                                                  68 of 100 random permutations                                                  69 of 100 random permutations                                                  70 of 100 random permutations                                                  71 of 100 random permutations                                                  72 of 100 random permutations                                                  73 of 100 random permutations                                                  74 of 100 random permutations                                                  75 of 100 random permutations                                                  76 of 100 random permutations                                                  77 of 100 random permutations                                                  78 of 100 random permutations                                                  79 of 100 random permutations                                                  80 of 100 random permutations                                                  81 of 100 random permutations                                                  82 of 100 random permutations                                                  83 of 100 random permutations                                                  84 of 100 random permutations                                                  85 of 100 random permutations                                                  86 of 100 random permutations                                                  87 of 100 random permutations                                                  88 of 100 random permutations                                                  89 of 100 random permutations                                                  90 of 100 random permutations                                                  91 of 100 random permutations                                                  92 of 100 random permutations                                                  93 of 100 random permutations                                                  94 of 100 random permutations                                                  95 of 100 random permutations                                                  96 of 100 random permutations                                                  97 of 100 random permutations                                                  98 of 100 random permutations                                                  99 of 100 random permutations                                                  100 of 100 random permutations                                                 Comparing empirical statistics with their null distributions... Please wait
#> ========================================================
#> Test of PCA significance: 2 variables, 101 observations
#> 100 bootstrap replicates, 100 random permutations
#> ========================================================
#> 
#> Empirical Psi = 2.0000, Max null Psi = 0.1442, Min null Psi = 0.0000, p-value = 0
#> Empirical Phi = 1.0000, Max null Phi = 0.2685, Min null Phi = 2e-04, p-value = 0
#> 
#> Empirical eigenvalue #1 = 2, Max null eigenvalue = 1.26854, p-value = 0
#> Empirical eigenvalue #2 = 0, Max null eigenvalue = 0.99981, p-value = 1
#> 
#> PC 1 is significant and accounts for 100% (95%-CI:100-100) of the total variation
#> 
#> Variables 1, and 2 have significant loadings on PC 1
```

<img src="man/figures/README-example2-1.png" width="100%" />
