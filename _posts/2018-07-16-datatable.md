---
layout: post
title: Introduction to data tables 
tags: [R, data.table]
#image: /img/hello_world.jpeg
---

If you're used to working in R, I'm sure you know *data.frame* from base R, a structure used for storing data in tables. There is a library that, from my point of view, offers the most efficient implementation of the aggregation logic in R, and the nicest and compressed syntax.

*data.table* objects behave in the same way as the base *data.frame*. However there are some differences not only related to syntax but also in programming efficiency. [*data.table*](https://cran.r-project.org/web/packages/data.table/data.table.pdf) offers fast and memory efficient: file reader and writer, aggregations, updates, equi, non-equi, rolling, range and interval joins, in a short and flexible syntax,for faster development

If you look for data.table help in google you'll find a looot of super useful websites, most of them better than this one. I'm sorry about that but this post is mainly for me, a way to collect the data.table theory. 

This post has been written based on this [*data.table* cheat sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/datatable_Cheat_Sheet_R.pdf)

```R
> library(data.table)

```
Creation of a data.table
```R
DT <- data.table(Shop=c(rep("A",5),rep("B",2),rep("C",5)),Units=1:12, Volume=c(1:8,NA,100,11,12)*10,
                 Mass=12:1*100, ClassID = c(rep("Premium",2),rep("LowCost",5),rep("Medium",2),rep("Premium",3)))
```
Overview of the data.table:
```R
> dim(DT)
> names(DT)
> head(DT)
> tail(DT)
> str(DT)
```

Once you know *data.table* you'll love it! Not only will you reduce the computing time in your programs, but also your programming time.


