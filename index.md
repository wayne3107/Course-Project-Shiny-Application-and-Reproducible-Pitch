---
title       : Basal metabolic rate calculation
subtitle    : 
author      : Zeng Mingwei
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Motivation

1. What is basal metabolic rate?
Basal metabolic rate (BMR) is the rate of energy expenditure by humans and other animals at rest.

2. Understand how much kcals your body needed in order to maitain the basic energy expenditure.

3. To keep you healthy you must fulfill this lowest standard.

---

## Harris-Benedict Equation

Several prediction equations exist. Historically, the most notable one was the Harris-Benedict equation:


for men,

13.7516 * weight + 5.0033 * height - 6.7550 * age + 66.4730

for women,

9.5634 * weight + 1.8496 * height - 4.6756 * age + 655.0955

---

## Shiny app

How it works?

1. Input your sex, age, height in cm, weight in kg.

2. Click 'Calculate!', the app will return your BMR.

---

## Shiny app

Example


```r
sex <- 'Male'
age <- 23
height <- 173
weight <- 59
BMR <- (sex=='Male')*(66.4730+13.7516*weight + 5.0033*height - 6.7550*age) + 
    (sex=='Female')*(655.0955 + 9.5634*weight + 1.8496*height - 4.6756*age)
BMR
```

```
## [1] 1588
```
