---
layout: page
permalink: /code/
title: code
description: 
---

My replication code and data can be accessed on [Harvard Dataverse](https://dataverse.harvard.edu/dataverse/seanhiggins).

My other code can be accessed on [GitHub](https://github.com/skhiggins/), including the packages I've written (described below).

### [Python packages](https://github.com/skhiggins/PythonTools/)

`get_files` automates downloading files from a website using web scraping when you provide it with a url and the file extensions to scrape.

`word2pdf` automates Microsoft Word document to pdf conversion.

`crop_eps` crops .eps files; useful when you can't get the cropping of a graph just right in your statistical software.

### [R packages](https://github.com/skhiggins/tabulator)

`tabulator` efficiently tabulates and produces Stata `tabulate`-like output. 

To install `tabulator` directly through R:
```r 
devtools::install_github("skhiggins/tabulator")
```

`tabulator` includes the following functions:
- `tab()` efficiently tabulates based on a categorical variable, sorts from most common to least common, and displays the proportion of observations with each value, as well as the cumulative proportion.
- `tabcount()` counts the unique number of categories of a categorical variable or formed by a combination of categorical variables.
- `quantiles()` produces quantiles of a variable. It is a wrapper for base R `quantile()` but is easier to use within `data.table`s or `tibble`s.
- `quo_to_chr()` works under the hood, converting a quosure to a character string.

### [Stata packages](https://github.com/skhiggins/StataTools)

To install directly through Stata:
```stata
ssc install <package_name>, replace
```

`ceq` is a [suite of commands](https://github.com/skhiggins/CEQStataPackage) to estimate fiscal incidence following the [Commitment to Equity](https://commitmentoequity.org/) framework.

`exampleobs` prints (randomly selected) example observations and optionally stores the values in a local macro. This is useful to explore possible values of a variable in your data set without being biased by the ordering of the data.

`fiscal_impoverishment` includes [commands](https://github.com/skhiggins/fiscal_impoverishment) to estimate fiscal impoverishment (FI) and fiscal gains to the poor (FGP), which are measures of how much the poor benefit from or are hurt by the tax and transfer system from [Higgins and Lustig (2016)](https://www.sciencedirect.com/science/article/pii/S0304387816300220). Additional commands graph FI and FGP curves. 

`head` prints the head observations (first observations in data set) and mimics the `head()` function in R and `head` command in Linux.

`randomselect` randomly selects observations and marks them with a dummy variable. It differs from `sample` in that it does not drop the non-selected observations from the data set, and that either individual observations or other units, defined by a variable in the data set, can be randomly selected.

`tail` prints the tail observations (last observations in data set) and mimics the `tail()` function in R and `tail` command in Linux.
​
