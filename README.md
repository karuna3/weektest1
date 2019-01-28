# weektest1
---
title: "Test"
author: "Test"
date: "January 28, 2019"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

```{r cars}
#Sequence of Numbers

#Creating a sequence of first 10 positive integers
seq(from = 1, to= 10)
seq(10)

#Creating a sequence of first 10 even numbers
seq(from = 2,by=2,length.out = 10)
seq(from = 2, to = 20, by=2)

#Creating a sequence of first 10 odd numbers
seq(from = 1,to = 19,length.out = 10)
seq(from = 1,to = 19, by = 2 )

#Creating a sequence of all odd numbers less than or equal to 87
seq(to = 87, by = 2)
seq(from = 1, to = 87, by = 2)

#Creating a sequence of based on length of input
seq(from = 1, to = 4, along.with = c("x","y","z"))
seq(from = 1, to = 10, along.with = c("w","x","y","z"))
```

```{r}
#Vectors

#Assigning a vector to a variable
X<-c(1,2,3,4,5)
print(X)

Y<-c(6,7,8,9,10)
print(Y)

#Math operations on two vectors
X+Y #It does an element by element addition
Y-X #It does an element by element substraction
X*Y #It does an element by element multiplication
Y/X #It does an element by element division

#Dealing with vectors of different size
w<-c(1,2,3,4)
z<-c(5,6)

#Smaller vector is repeated
w+z 
w-z
w*z
w/z
```

```{r}
#Missing Data

#Checking if the data has any missing values
x<-NA
is.na(x)

y<-c(1,2,3,NA,4,NA,5)
is.na(y)

#Excluding missing data from analysis
sum(y) #Returns NA as the vector contains NA
mean(y)
sum(y, na.rm = TRUE) #Excludes NAs while performing the operations
mean(y, na.rm = TRUE)

#Removing NAs from your vector
na.omit(y)
na.omit(x)

#Replace NAs with another value
replace(y,is.na(y),0)
replace(x,is.na(x),-1)
```

```{r}
#Subsetting Vectors
x<-c(1.1,2.2,3.3,4.4,5.5)

#Blank returns all the values
x[]

#Access values at specific location
x[1]
x[4]

#Access values at more than one location
x[c(2,5)]
x[c(3,1)]

#Access sequential values in a vector
x[1:4]
x[2:5]

#Omitting values
x[-1]
x[-c(2,5)]

#Logical operators to select or reject elements
x[c(TRUE)]
x[c(TRUE,FALSE)]
x[c(TRUE,TRUE,FALSE,FALSE,TRUE)]
```

```{r}
#Matrices and Data Frames
#Create a matrix
x<-matrix(1:12,nrow = 3, ncol = 4)
print(x)

#Create a data frame
y<-as.data.frame(matrix(1:9,nrow = 3,ncol = 3))
#Assign column names
colnames(y)<-c("Column1","Column2","Column3")
print(y)

#Arithmetic operations on matrices and data frames
x+1 #Each element is incremented by 1
y-1 #Each element is decremented by 1

#Access a particular cell in matrix or data frame
x[2,3] #2nd row and 3rd column
y[1,1] #1st row and 1st column

#Replacing NAs in a data frame
z<-as.data.frame(matrix(c(1,2,NA,3,NA,4,NA,NA,5),nrow = 3,ncol = 3))
print(z)

z[is.na(z)]<-0
print(z)
```


Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
