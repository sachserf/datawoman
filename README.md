# datawoman

The goal of datawoman is to facilitate some data manipualtion tasks.

## Installation

You can install datawoman from github via:

```R
devtools::install_github("sachserf/datawoman")
```

## Example

### COMpare COMmon COLumns - comcomcol()
- Functional for different tasks:

#### compare class
- e.g. useful just before combining similar dataframes 
```R
foo <- iris
foo[, sapply(foo, is.factor)] <- sapply(foo[, sapply(foo, is.factor)], as.character)
bar <- iris[, 2:5]
datawoman::comcomcol(foo, bar, iris)
```

#### compute mean for each variable in a single dataframe
```R
datawoman::comcomcol(mtcars, custom_fun = mean)
```
