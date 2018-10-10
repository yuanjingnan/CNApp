# CNApp ##
CNApp is a comprehensive shiny-based web application to perform copy number alterations (CNAs) analysis in a user-friendly interface. CNApp generates genome-wide CNA profiles, calculates focal and broad CNA scores, and establishes associations with molecular and clinical features. Furthermore, machine learning-based prediction models classify samples by multiple parameters generated by the software. 
CNApp provides a unique scenario to comprehensively analyze CNAs and integrate them with molecular and clinical features.

Please give credit and cite CNApp when you use it for your integrative CNA analysis XXXX.

## Running the app ##

First __check dependencies needed to run CNApp__ by copying the following code in R (or RStudio):


```R

if(!require(shiny)) install.packages("shiny")
if(!require(shinyBS)) install.packages("shinyBS")
if(!require(shinyjs)) install.packages("shinyjs")
if(!require(shinythemes)) install.packages("shinythemes")
if(!require(shinyWidgets)) install.packages("shinyWidgets")
if(!require(shinydashboard)) install.packages("shinydashboard")

if(!require(V8)) install.packages("V8")
if(!require(plotly)) install.packages("plotly")
if(!require(randomcoloR)) install.packages("randomcoloR")
if(!require(heatmaply)) install.packages("heatmaply")
if(!require(ggplot2)) install.packages("ggplot2")
if(!require(ggsignif)) install.packages("ggsignif")
if(!require(RColorBrewer)) install.packages("RColorBrewer")
if(!require(randomForest)) install.packages("randomForest")
if(!require(doBy)) install.packages("doBy")
if(!require(parallel)) install.packages("parallel")
if(!require(caret)) install.packages("caret")
if(!require(XML)) install.packages("XML")

if (!require(devtools)) install.packages("devtools")

if(!require(limma)) {source("http://www.bioconductor.org/biocLite.R");biocLite("limma")}

if(!require(GenomicFeatures)) {source("http://www.bioconductor.org/biocLite.R");biocLite("GenomicFeatures")}
if(!require(GenomicAlignments)) {source("http://www.bioconductor.org/biocLite.R");biocLite("GenomicAlignments")}
if(!require(GenVisR)) {source("http://www.bioconductor.org/biocLite.R");biocLite("GenVisR")}

if(!require(shinysky)) {library(devtools); devtools::install_github("AnalytixWare/ShinySky")}
if(!require(GenVisR)) {library(devtools); devtools::install_github("griffithlab/GenVisR")}

if (!require(webshot)) install.packages("webshot")

if(!require(phantomjs)) {webshot::install_phantomjs()}

```
**If warning outputs are printed, try again!**
**(or try line by line...)**


There are many ways to download and run CNApp:

Run from GitHub repository:

```R
# Easiest way is to use runGitHub to run CNApp from GitHub:
library(shiny)
runGitHub("CNApp", "ait5")
```

By loading CNApp from compressed app url:

```R
# Run a tar or zip file directly
runUrl("https://github.com/ait5/CNApp/archive/master.tar.gz")
runUrl("https://github.com/ait5/CNApp/archive/master.zip")
```
By cloning or downloading repository:
```
# Using runApp(),  first clone the repository with git. If you have cloned it into
# ~/CNApp, first go to that directory, then use runApp().
setwd("~/CNApp")
runApp()
```

