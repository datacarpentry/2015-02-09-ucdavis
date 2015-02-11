R Challenge Questions, Day 1
========================================================

Challenge
=========

Based on the output of `str(surveys)`, can you answer the following questions?

* What is the class of the object `surveys`?
* How many rows and how many columns are in this object?
* How many species have been recorded during these surveys?

Challenge
=========

The function `table()` tabulates observations and can be used to create
bar plots quickly. can you recreate this plot but by having "control" being listed last instead of first?


```r
exprmt <- factor(c("treat1", "treat2", "treat1", "treat3", "treat1", "control",
                   "treat1", "treat2", "treat3"))
table(exprmt)
```

```
exprmt
control  treat1  treat2  treat3 
      1       4       2       2 
```

```r
barplot(table(exprmt))
```

![plot of chunk unnamed-chunk-1](r-challenge-questions-day-1-figure/unnamed-chunk-1-1.png) 

Challenge
=========

Spot and fix the errors in this hand-crafted data frame.


```r
author_book <- data.frame(
	author_first=c("Charles", "Ernst", "Theodosius"),
  author_last=c(Darwin, Mayr, Dobzhansky),
  year=c(1942, 1970))
```

Challenge
=========

Predict the class for each of the columns in the following example. Check your gueses using `str(country_climate)`


```r
country_climate <- data.frame(
  country=c("Canada", "Panama", "South Africa", "Australia"),
  climate=c("cold", "hot", "temperate", "hot/temperate"),
  temperature=c(10, 30, 18, "15"),
  north_hemisphere=c(TRUE, TRUE, FALSE, "FALSE"),
  has_kangaroo=c(FALSE, FALSE, FALSE, 1))
```

Challenge
=========

The function `nrow()` on a `data.frame` returns the number of rows. 

Use it,
in conjuction with `seq()` to create a new `data.frame` called
`surveys_by_10` that includes every 10th row of the survey data frame
starting at row 10 (10, 20, 30, ...)
