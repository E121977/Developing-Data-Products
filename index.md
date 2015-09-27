---
title       : "DDP Project - Word Cloud"
subtitle    : Edgar Allen Poe works analysis
author      : "E121977"
job         : Slidify Project for Coursera Developing Data Products
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

The pupose of this project is to provide a tool that will show the user
a word cloud text analysis of popular works by Edgar Allen Poe. This may
seem trival, but could prove to a powerful analysis tool depending on 
the type and size of the data sources. Large text data files can be
transformed into visual patterns showing key areas of significance. 
This technique is utilized daily in many business segments and industries.
<br>
<br>
# **Word Cloud:**
<br>
**"An image composed of words use in a particular text or subject, 
in which the size of each word indicates the frequency or importance."** 

--- 

## Methodology
First we will load a known list of valid books. This can be extened to whatever texts you wish to analyze.

```r
# The list of valid books.
books <<- list("The Fall of the House of Usher" = "Usher.txt",
              "The Raven" = "Raven.txt",
              "The Masque of the Red Death" = "Death.txt",
              "The Works of Edgar Allan Poe" = "Works.txt")
```
The application takes advantage of the **memoise** package. This package allows us to cache resutls for faster processing once the code is run initally. This function will create a Document Term Matrix that the **tm** package uses to determine statistics on the text.


<!--Inside the function we will place the following code that will actually process the text and compute the statistics. -->



---

## Shiny
We now have code that computes some intersting statistics on our text. The next step is to deliver an easy to use  application to our customer who may not have experience with R or may not have any technical expertise. We will use the shiny package to create a web application that wraps an easy to use interface over our code. The user can easily view and adjust the statistics. This approach reqires three basic files: 
- global.R (our processing code)
- server.R (the code instructions required to build the application)
- ui.R (the code supporting the UI functions of the web application)


The code for the files can be found at: https://github.com/E121977/DDP-Word-Cloud-Shiny-Application 

You can find the application here: https://e121977kb.shinyapps.io/DDP-Word-Cloud

---

## Conclusion
If you need to provie insight or actionable information to your organization you can 
present it in a very usable format thorugh the use of the following tools:
<br>
- R: Peform your data science and analytics.
- Shiny: Provide your user interface to provide useful tools to manipulate the data.
- Slidify/Knitr/R Presentation: Provide documentation and presentation of your findings.
<br>
<br>

# Enjoy the Experience and Share the Shiny Fun!!!



