Intro to R
========================================================
author: Darya Akimova
date: 9/14/2017
width: 1440
height: 900

N-Languages Meetup


Who am I?
========================================================

- BA in Biochemistry and Molecular Biology

- PhD Candidate in Pharmacology

- Research project focused on computational metabolomics


Who uses R?
========================================================

![alt text](r_use.png)

<small>Credit: David Robinson (Stack Overflow), 2017 New York R Conference</small>


What is R?
========================================================

- Interpreted, statistical programming language
- First appeared in 1993
- Primarily for:
    + Data processing / munging / wrangling
    + Analysis
    + Visualization
    + Communication


R Competition
========================================================

- Python
- Julia
- SAS
- SPSS
- MATLAB


R Basics
========================================================


```r
"Hello, World!"
```

```
[1] "Hello, World!"
```

Assignment:

```r
right.var <- "use this"
wrong.var = "don't use this"
```

Naming Conventions:


```r
this_is_ok <- "good"
this.is.also.ok <- "good"
someUseThis <- "good"
```


Data types in R
========================================================


```r
class(9)
```

```
[1] "numeric"
```

```r
class("word")
```

```
[1] "character"
```

```r
class(factor(1, levels = 1))
```

```
[1] "factor"
```

```r
v <- c(1, "b", 3)
class(v)
```

```
[1] "character"
```


Data types in R
========================================================


```r
m <- matrix(c(1,2,3,4), ncol = 2, nrow = 2)
class(m)
```

```
[1] "matrix"
```

```r
m
```

```
     [,1] [,2]
[1,]    1    3
[2,]    2    4
```
***

```r
d <- data.frame(c(1, 2, 3), c("a", "b", "c"))
colnames(d) <- c("num", "char")
class(d)
```

```
[1] "data.frame"
```

```r
d
```

```
  num char
1   1    a
2   2    b
3   3    c
```

```r
sapply(d, class)
```

```
      num      char 
"numeric"  "factor" 
```


Basic math in R
========================================================

Base R can take you very far in data analysis.
Calculator:

```r
3 + 2
```

```
[1] 5
```

```r
3 * 2
```

```
[1] 6
```

```r
3 / 2
```

```
[1] 1.5
```
***

```r
3 ^ 2
```

```
[1] 9
```

```r
3 %% 2
```

```
[1] 1
```

```r
class(3)
```

```
[1] "numeric"
```

```r
class(3 / 2)
```

```
[1] "numeric"
```


If Else
========================================================


```r
x <- "word"
if (class(x) == "numeric") {
  "It's a number!"
} else if (class(x) == "character") {
  "It's a word!"
} else {
  "I don't know"
}
```

```
[1] "It's a word!"
```


Functions in R
========================================================


```r
NumberSquared <- function(number) {
  ans <- number ^ 2
  return(ans)
}
x <- 2
NumberSquared(x)
```

```
[1] 4
```


For loops in R
========================================================

Similar to other languages: 

```r
for (i in 1:5) {
  print(i)
}
```

```
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
```

But really you should use the apply family of functions:
- apply
- sapply
- lapply
- etc.


Data analysis tools built in
========================================================


```r
x <- 1:10
mean(x)
```

```
[1] 5.5
```

```r
median(x)
```

```
[1] 5.5
```

```r
quantile(x)
```

```
   0%   25%   50%   75%  100% 
 1.00  3.25  5.50  7.75 10.00 
```


Building on the R {base}
========================================================

- Package: an organized collection of functions, code, or data 

- Can be stand alone or build on other packages

- To call a package: library(package) or require(package)

- Be careful loading


3 Places where R packages live
========================================================

- CRAN: 
  + install.packages("package_name")

- Bioconductor: https://bioconductor.org/ 
  + source("https://bioconductor.org/biocLite.R")
  + biocLite("package_name")

- Github:
  + library(devtools)
  + install_github("repo/package_name")
  
- rOpenSci Project
  + https://ropensci.org/
  
  
There are a lot of R packages
========================================================

For better or worse

![alt text](1vrn1f.jpg)


Popular packages
========================================================

![alt text](r_pop_packages.png)

<small>Credit: David Robinson (Stack Overflow), 2017 New York R Conference</small>


Hadley Wickham
========================================================

![alt text](Hadley-wickham2016-02-04.jpg)


Tidyverse is about tidy data
========================================================

Philosophy of what clean data should look like:
- Variables in columns
- Each observation/sample is a row
- Each type of observational unit is a table 

R packages built around:
- Tibble (alternative to data frame)
- Getting your data or results into the tidy format
- Working with tidy data


{base} versus {tidyverse}
========================================================

![alt text](1vrkzw.jpg)


Ways to communicate with R
========================================================

- R Markdown files (produces HTML, PDF, Word)
- Shiny (interactive documents)
- R Presentation
- Bookdown / Blogdown
- Jupyter Notebooks


Useful resources
========================================================

- Learning base R: swirl package http://swirlstats.com/
- R for Data Science by Hadley Wickham http://r4ds.had.co.nz/
- R Cheatsheets https://www.rstudio.com/resources/cheatsheets/
- ggplot2 cookbook http://www.cookbook-r.com/Graphs/

Thanks for your time
========================================================

(I'm not hiring)

Questions?
