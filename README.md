# Course-MOGEN
---
title: "RC CH3+CH4: Site specific recombination and Horizontal gene transfer"
output: html_document
author: Sofie Thijs (sofie.thijs@uhasselt.be)
date: 20/10/2020
theme: cerulean
---

<style type="text/css">

body{ /* Normal  */
      font-size: 14px;
  }
td {  /* Table  */
  font-size: 18px;
}
h1.title {
  font-size: 38px;
  color: Purple;
}
h1 { /* Header 1 */
  font-size: 28px;
  color: DarkBlue;
}
h2 { /* Header 2 */
    font-size: 22px;
  color: DarkBlue;
}
h3 { /* Header 3 */
  font-size: 18px;
  font-family: "Times New Roman", Times, serif;
  color: DarkBlue;
}
code.r{ /* Code block */
    font-size: 12px;
}
pre { /* Code block - determines code spacing between lines */
    font-size: 14px;
}
</style>


&nbsp;
&nbsp;
&nbsp;


Here you will find the questions and resources to go through the various course topics related to mechanisms that induce genetic variation, repair, and to get familiar with their biotechnological applications.


![](http://www.australasianscience.com.au/sites/default/files/imagecache/article_main_image/DNA_evolution.jpg)</center>

```{r knitr, include=FALSE}
knitr::opts_chunk$set(
	echo = TRUE,
	message = FALSE,
	warning = FALSE,
	eval = TRUE
)
#ref for the font: https://stackoverflow.com/questions/30446905/rmarkdown-font-size-and-header/30447045
```

``` {r cleanup, include=FALSE}
rm(list=ls()) # remove all objects from your workspace, start clean
options(warn=-1) # toggle off warnings
```

```{r setup, include=FALSE}
### libraries
library(lifecycle)
library(tidyverse)
library(yaml)
library(icesTAF)
library(rmarkdown)
library(renv)
library(knitr)
library(kableExtra)
```

# Schedule
```{r read schedule, echo=FALSE}
# ref: https://rmd4sci.njtierney.com/using-rmarkdown.html
schedule <- read_csv("G:/My Drive/1.Sofie/1.Onderwijs/Bachelor/MoleculaireGenetica/20_21/LessenSofie/CH5/schedule.csv")
topschedule <- head(schedule)
urls <- rep("http://stackoverflow.com/",6)
topschedule$Activity <- paste0("[",topschedule$Activity, "](", urls, ")")
knitr::kable(topschedule, "html")%>%
  kable_styling("striped", full_width=FALSE, font_size = 25, position = "left")
```


## Learning outcomes
By the end of the RC, you should be able to:  

- Explain what GATEWAY Cloning Technology is and on which natural mechanism it is based. You know that there are different GATEWAY expression vector systems, and you can give an example of how GATEWAY cloning is used.  

- You can understand and discuss transposable elements in eukaryotes, and how it has contributed to genetic diversity  

- You know how to use web-based databases for searching transposons, IS, CRISPR repeats in bacteria, fungi, plant cells.  

- You can schematise the process of CRIPRcas9, give an example of an application, and you can discuss prime editing.


## Course instructor
Sofie.thijs@uhasselt.be
