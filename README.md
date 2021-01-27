# Air-pollution-programming-assignment (orginal url from coursera: https://www.coursera.org/learn/r-programming/supplement/amLgW/programming-assignment-1-instructions-air-pollution)

## Introduction
For this first programming assignment you will write three functions that are meant to interact with dataset that accompanies this assignment. The dataset is contained in a zip file specdata.zip that you can download from the Coursera web site. 

Although this is a programming assignment, you will be assessed using a separate quiz.

Data
The zip file containing the data can be downloaded here:

specdata.zip [2.4MB] https://d396qusza40orc.cloudfront.net/rprog%2Fdata%2Fspecdata.zip
The zip file contains 332 comma-separated-value (CSV) files containing pollution monitoring data for fine particulate matter (PM) air pollution at 332 locations in the United States. Each file contains data from a single monitor and the ID number for each monitor is contained in the file name. For example, data for monitor 200 is contained in the file "200.csv". Each file contains three variables:

Date: the date of the observation in YYYY-MM-DD format (year-month-day)
sulfate: the level of sulfate PM in the air on that date (measured in micrograms per cubic meter)
nitrate: the level of nitrate PM in the air on that date (measured in micrograms per cubic meter)
For this programming assignment you will need to unzip this file and create the directory 'specdata'. Once you have unzipped the zip file, do not make any modifications to the files in the 'specdata' directory. In each file you'll notice that there are many days where either sulfate or nitrate (or both) are missing (coded as NA). This is common with air pollution monitoring data in the United States.

### Part 1
Write a function named 'pollutantmean' that calculates the mean of a pollutant (sulfate or nitrate) across a specified list of monitors. The function 'pollutantmean' takes three arguments: 'directory', 'pollutant', and 'id'. Given a vector monitor ID numbers, 'pollutantmean' reads that monitors' particulate matter data from the directory specified in the 'directory' argument and returns the mean of the pollutant across all of the monitors, ignoring any missing values coded as NA. 


You can see some example output from this function below. The function that you write should be able to match this output. Please save your code to a file named pollutantmean.R.

pollutantmean-demo.html
https://d3c33hcgiwev3.cloudfront.net/_3b0da118473bfa0845efddcbe29cc336_pollutantmean-demo.html?Expires=1611878400&Signature=eZ~WnsCSzpNeDi-iJckizCIJZxvnpf4XtFvGG9moPBAcJ5KSdM4cOz8OKXIxcBY4JFtKSqT-LhYabWs3Cpx1f5vty-zj-PHe3TBc7p-N11xcOYYqA~Z95FD9vO4unVEPq2-TgEBwwaMfv1ajJeO5PRLPW~7DuNM0HB9Zn~8~eIo_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A


### Part 2
Write a function that reads a directory full of files and reports the number of completely observed cases in each data file. The function should return a data frame where the first column is the name of the file and the second column is the number of complete cases. 


You can see some example output from this function below. The function that you write should be able to match this output. Please save your code to a file named complete.R. To run the submit script for this part, make sure your working directory has the file complete.R in it.

complete-demo.html
https://d3c33hcgiwev3.cloudfront.net/_3b0da118473bfa0845efddcbe29cc336_complete-demo.html?Expires=1611878400&Signature=eGO0QONWybqCd3KuqLcmj7j6ylZeyApfz95euH5M-dIOXzOHST9djC1T8TK~ejEvozPZrZn~eLmc8naEakEtIGHmVM2ATxPoMEqYoBPP3bFAaL6cUFK7bcdAnHZ1GZv-yDssivRlgKrr0qcQGefKJSZDsgf4DaB56D5ttKDKIx0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A



### Part 3
Write a function that takes a directory of data files and a threshold for complete cases and calculates the correlation between sulfate and nitrate for monitor locations where the number of completely observed cases (on all variables) is greater than the threshold. The function should return a vector of correlations for the monitors that meet the threshold requirement. If no monitors meet the threshold requirement, then the function should return a numeric vector of length 0. 


For this function you will need to use the 'cor' function in R which calculates the correlation between two vectors. Please read the help page for this function via '?cor' and make sure that you know how to use it.

You can see some example output from this function below. The function that you write should be able to approximately match this output. Note that because of how R rounds and presents floating point numbers, the output you generate may differ slightly from the example output. Please save your code to a file named corr.R. To run the submit script for this part, make sure your working directory has the file corr.R in it.

corr-demo.html
https://d3c33hcgiwev3.cloudfront.net/_e92e575b8e62dcb1e3a086d2ff0d5a1e_corr-demo.html?Expires=1611878400&Signature=RTlTZ8zq5qS-xgfWw47FF91Ebh1FBH1LkXz7DyF6zzpbZfbhzQwGpBppDzc9Fh2nTHSWPdnJ7m3tjzXC0CpZ5k7fxj2sGHyUL1KLV1zmkW11fRC37bRYGbSubOnCXrxG~obeeEtmpTpLEwLvnM-DdQ5fqphdFs2TICjXm6CVj6w_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A

Grading
This assignment will be graded using a quiz.

