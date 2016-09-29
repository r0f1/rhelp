# R help

## Exploratory data analysis

### Finding out n, distribution

    library(psych)
    cols <- c("n", "mean", "median", "min", "max", "sd")
    desc <- data.frame(describe(dt))[cols]

More info see [here](http://www.statmethods.net/stats/descriptives.html) and [here](http://www.ats.ucla.edu/stat/r/faq/collapse.htm).


## Reliably importing packages

    packages <- c("xtable", "stats", "plyr", "dplyr", "ggplot2", "RColorBrewer")
    
    for(i in 1:length(packages)) {
    	pkg <- packages[i]
    	if (!require(pkg, character.only=TRUE)) {
    		install.packages(pkg, repos="http://cran.rstudio.com/")
    		library(pkg, character.only=TRUE)
    	}
    }
