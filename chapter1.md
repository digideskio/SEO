---
title       : Import your data crawl
description : Screaming Frog, Botify, Deepcrawl, Oncrawl, Kelogs
attachments :
  slides_link : http://www.screamingfrog.co.uk/seo-spider/

--- type:VideoExercise lang:r xp:30 skills:1 key:a5f5fbf146
## Visits 

--- type:NormalExercise lang:r xp:50 skills:1 key:7ccf59caa3
## Structure et Comprehension

Nous allons analyser la structure du dataframe urls qui est préchargé dans votre workspace. Pour cela utilisez la fonction str(). La fonction prend en paramètre, le dataframe.

*** =instructions

Lancer la commande str() sur votre data_frame.

*** =hint
Avez-vous utiliser str(votre_data_frame) ?

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace. You can use it for several things:

# 2. Pre-load packages, so that users don't have to do this manually.
library(readxl)

# 1. Preload a dataset. The code below will read the csv that is stored at the URL's location.
# The movies variable will be available in the user's console.
urls <-  read.csv("http://wordpress-logs-vincent59.c9users.io/csv/crawl-scifi.csv", header = TRUE, sep=";")

```

*** =sample_code
```{r}
# write str



```

*** =solution
```{r}
# write str
str(urls)
```


*** =sct
```{r}
# The sct section defines the Submission Correctness Tests (SCTs) used to
# evaluate the student's response. All functions used here are defined in the 
# testwhat R package. Documentation can also be found at github.com/datacamp/testwhat/wiki

# Test whether the function str is called with the correct argument, object
# If it is not called, print something informative
# If it is called, but called incorrectly, print something else
test_function("str", args = "object",
              not_called_msg = "You didn't call `str()`!",
              incorrect_msg = "You didn't call `str(object = ...)` with the correct argument, `object`.")

# Test the object, good_movies
# Notice that we didn't define any feedback here, this will cause automatically 
# generated feedback to be given to the student in case of an incorrect submission
test_object("urls")

# It's always smart to include the following line of code at the end of your SCTs
# It will check whether executing the student's code resulted in an error, 
# and if so, will cause the exercise to fail
test_error()

# Final message the student will see upon completing the exercise
success_msg("Good work!")

```

--- type:NormalExercise lang:r xp:200 skills:1 key:2393503932
## Level and Sessions

In the previous exercise, you saw a dataset about urls.

A dataset with a selection of urls, `urls`, is available in the workspace.

*** =instructions
- Check out the structure of `urls`
- Select Level and Sessions of `urls`. Stored data in small_urls
- aggregate your data with the level and store results in urls_level. Insert list(Level=urls_select$Level) onto by, sum onto FUN

*** =hint
- Use `str()` for the first instruction.
- Use select() instruction.
- Use aggregate() instructions on GA.Sessions


*** =pre_exercise_code
```{r}
# Pre-load a package in the workspace
library(dplyr)
urls <-  read.csv("http://wordpress-logs-vincent59.c9users.io/csv/crawl-scifi.csv", header = TRUE, sep=";")
```

*** =sample_code
```{r}
# write str on urls data


# select level and sessions and stored data in a new data frame : small_urls


# aggregate your data. Use small_urls dataframe. Store results in urls_level


```

*** =solution
```{r}
# write str
str(urls)

# select level and sessions and stored data in a new data frame : small_urls
small_urls <- select(data = urls, Level, GA.Sessions)

# aggregate your data. Use small_urls dataframe
urls_level <- aggregate(small_urls$GA.Sessions, by=list(Level=small_urls$Level), FUN=sum)

```

*** =sct
```{r}
# The sct section defines the Submission Correctness Tests (SCTs) used to
# evaluate the student's response. All functions used here are defined in the 
# testwhat R package. Documentation can also be found at github.com/datacamp/testwhat/wiki

# Test whether the function str is called with the correct argument, object
# If it is not called, print something informative
# If it is called, but called incorrectly, print something else
test_function("str", args = "object",
              not_called_msg = "You didn't call `str()`!",
              incorrect_msg = "You didn't call `str(object = ...)` with the correct argument, `object`.")

# Test the object, good_movies
# Notice that we didn't define any feedback here, this will cause automatically 
# generated feedback to be given to the student in case of an incorrect submission
test_object("urls")

test_function("select", args = "object",
              not_called_msg = "You didn't call `select()`!",
              incorrect_msg = "You didn't call `select(object = ...)` with the correct argument, `object`.")
              
# Alternativeley, you can use test_function() like this
# test_function("select", args = c("data"))
              
test_object("small_urls")   

test_function("aggregate", args = "object",
              not_called_msg = "You didn't call `aggregate()`!",
              incorrect_msg = "You didn't call `aggregate(object = ...)` with the correct argument, `object`.")

# test_function("select", args = c("x", "by", "FUN"))
              
test_object("urls_level")   


# It's always smart to include the following line of code at the end of your SCTs
# It will check whether executing the student's code resulted in an error, 
# and if so, will cause the exercise to fail
test_error()

# Final message the student will see upon completing the exercise
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:69eabaa8f8
## Performance

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```


--- type:NormalExercise lang:r xp:100 skills:1 key:e8cb166fde
## HTTP Codes

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```

--- type:NormalExercise lang:r xp:100 skills:1 key:b2cc06531b
## HTTP Tags

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```

--- type:NormalExercise lang:r xp:100 skills:1 key:4285739ca6
## Inlinks

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```

--- type:NormalExercise lang:r xp:100 skills:1 key:f3132dda60
## Outlinks

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```

--- type:NormalExercise lang:r xp:100 skills:1 key:07a7a622ec
## Alerts

*** =instructions
- inst1

*** =hint
- hint1

*** =solution
```{r}
```

