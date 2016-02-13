DevelopingDataProducts-Course Project App for Mileage Calculation and Cars Comparison
========================================================
author: aroyyuru
date:  13 Feb 2016
autosize: true

Project Data And its links (Overview)
========================================================

This was built as part of a deliverable for the course Developing Data Products as part of the Coursera Data Science Specialization.

The app developed for the first part of the assignment demo is avalilable at: https://aroyyuru.shinyapps.io/DevelopingDataProducts-CourseProject/

Source code for ui.R and server.R files are available on the GitHub repo: https://github.com/aroyyuru/DevelopingDataProducts


Web Application functionality
========================================================

This app is a tool to select the best car for your trip.

We required you provide your trip detail like distance of your trip and the price od gasoline in your region, it's needed to calculate the Gasoline Expenditure for each car. Next with provide your budget on gasoline, so we can filtered and show the car with has Miles per Gallon(MPG) that below your budget.

Second, you can choose your desire cars characteristic in term of : Cylinders, Displacement, Horse Power and Transmission.

The result contains filters selected cars will show in a table on the main content with using the mtcars dataset.


MTCARS Dataset
========================================================
The data used in the app comes from the Motor Trend Car Road Tests (mtcars) dataset. Let has a look on the mtcars's summary

 head(mtcars)


```r
## Car Make/Model    mpg  cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```

Plot
========================================================
Here we can see the relationship between three variables: miles per gallon (mpg), displacement (disp) and weight (wt).

   
   ```r
     library(car)
     scatterplot.matrix(~mpg+disp+wt, data=mtcars, cex.axis=1.5)
   ```
   
   ![plot of chunk unnamed-chunk-2](DevelopingDataProducts-figure/unnamed-chunk-2-1.png)


