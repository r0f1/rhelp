# R help

## Reliably importing packages

    packages <- c("xtable", "stats", "plyr", "dplyr", "ggplot2", "RColorBrewer")
    
    for(i in 1:length(packages)) {
    	pkg <- packages[i]
    	if (!require(pkg, character.only=TRUE)) {
    		install.packages(pkg, repos="http://cran.rstudio.com/")
    		library(pkg, character.only=TRUE)
    	}
    }
    