# Title

Title

## Usage

``` r
istl(
  y,
  periods,
  multiplicative = TRUE,
  swindows = NULL,
  twindows = NULL,
  ninnerloop = 1,
  nouterloop = 15,
  nojump = FALSE,
  weight.threshold = 0.001,
  weight.function = c("BIWEIGHT", "UNIFORM", "TRIANGULAR", "EPANECHNIKOV", "TRICUBE",
    "TRIWEIGHT")
)
```

## Arguments

- weight.function:

## Examples

``` r
q<-rjd3stl::istl(rjd3toolkit::ABS$X0.2.09.10.M, c(12, 25))
#> Error in .jcall("jdplus/stl/base/r/StlDecomposition", "Ljdplus/toolkit/base/api/math/matrices/Matrix;",     "istl", as.numeric(y), .jarray(as.integer(periods)), as.logical(multiplicative),     swin, twin, as.integer(ninnerloop), as.integer(nouterloop),     as.logical(nojump), as.numeric(weight.threshold), as.character(weight.function)): java.util.ServiceConfigurationError: jdplus.toolkit.base.api.information.InformationExtractor: Provider jdplus.stl.base.core.stlplus.extractors.MStlPlusExtractor could not be instantiated
decomp<-q$decomposition
#> Error in q$decomposition: object of type 'closure' is not subsettable
matplot(decomp[,c(1:3)], type='l')
#> Error: object 'decomp' not found
```
