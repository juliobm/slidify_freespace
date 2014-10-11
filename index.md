---
title       : Coursersa Project Developing Data Products 
subtitle    : Free Space on disks Server
author      : Julio B-M
job         : TIC responsible
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## The problem and solution

* I'm responsible of many servers of a company. I'm fear about getting low space on disks.  
* In Sep-2011 I made a python script that checks every fex minutes free space on disks on each server of my lan and logs in a file once a day the result.   
* If a disk gets 1GB low, the script sends me a email.  

**Now I want to see the log-data I got along these years graphically**.



--- .class #id 

## The data


The log file has this structure

```r
datalog <- read.csv("libre_en_disco_log.csv", dec=",",head=TRUE,sep="\t")
head(datalog)
```

```
##          SERVIDOR DISCO      FECHA     HORA     GB
## 1        S_SHADOW    E$ 2014-09-29 08:10:00  12.97
## 2        S_SHADOW    C$ 2014-09-29 08:10:00   2.35
## 3        INTRANET    C$ 2014-09-29 08:10:00   2.08
## 4            S_TS    C$ 2014-09-29 08:10:00  35.93
## 5 BU-CONCENTRADOR    C$ 2014-09-30 08:10:00 191.07
## 6            VWEB    C$ 2014-09-30 08:10:00  20.09
```

--- .class #id

## The ShinyApp


* I made this shinyapp  

https://juliobm.shinyapps.io/shiny_freespace

* You can choose server and the the page shows you only the disks that has the server.

* You can select a range date to show the data too.

* In another tab you can see the log file in table format.

* You can see the code at this link

https://github.com/juliobm/slidify_freespace



--- .class #id

## A graph example

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2.png) 
