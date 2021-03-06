---
title       : Predicting Your Score for The Data Products Course
subtitle    : Just for Fun =)
author      : Author A
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

1. This little application attempts to predict your score for the data products course
2. This is useful to give the user a gauge whether if he / she is going to pass the course
3. The objective is to let the user know, "hey it is time to work harder" or "you are doing well"

--- .class #id 

## 3 Questions

The prediction is simple and asked the user to answer 3 questions:
* Do you find the course difficult?
* Do you intend to do the course project?
* On average what is your quiz score (Normalize it to 1 - 10)


--- .class #id 

## Marking Criteria

A score is given for each question that is answered. Specifically,
* Do you find the course difficult? --> 1 mark is given for "No"
* Do you intend to do the course project? --> 1 mark is given for yes
* On average what is your quiz score (Normalize it to 1 - 10) --> 1 mark is given for >7

--- .class #id 

## An Example

Based on the score, the user is given a remark. An example is given below:


```r
score <-0
 if (score == 3){
    results <-'I am sure you will pass'
  }else if (score >= 1){
    results <- 'Work harder and you might pass'
  }else{
    results <- 'Hmm, Roger Peng will be upset'
  }
results
```

```
## [1] "Hmm, Roger Peng will be upset"
```

