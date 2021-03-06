# rBR

The rBR package aims to help with brazilian numbers used to identify companies and individuals (CNPJ and CPF, for example).

The package provides functions to validate, format and execute comparisons of these numbers when they come in different formats, for example, compare a numeric CPF against a character CPF.
The functions are implemented in a vectorized way in order to speed up validations and comparison in large datasets.

## Install

The package can be installed directly from github using devtools.

```{r}
devtools::install_github('wilsonfreitas/rBR')
```

## Using

The numbers can be created with numeric or character vectors:

```{r}
> x <- CNPJ(13515463000138)
> x
13.515.463/0001-38 
> is.valid(x)
[1] TRUE
> x == 13515463000138
[1] TRUE
> x <- CPF(c("681.943.594-06", "012.391.576-73", "520.082.755-82"))
> x
681.943.594-06 012.391.576-73 520.082.755-82 
> is.valid(x)
[1] TRUE TRUE TRUE
> x == 68194359406
[1]  TRUE FALSE FALSE
```

## Contribute

For now we have CPF and CNPJ implemented, so if you need another number or, even better, if you have it implemented, get in touch so we can add new numbers to the package.
