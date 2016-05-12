---
title       : Import your data crawl
description : Screaming Frog, Botify, Deepcrawl, Oncrawl, Kelogs
attachments :
  slides_link : http://www.screamingfrog.co.uk/seo-spider/

--- type:VideoExercise lang:r xp:30 skills:1 key:a5f5fbf146
## Visits 

*** =video_link
//player.vimeo.com/video/154783078

--- type:MultipleChoiceExercise lang:r xp:50 skills:1 key:7ccf59caa3
## Distribution

We are going to analyse Apache logs

*** =instructions
Vous devez charger le fichier xlsx de Screaming Frog

*** =hint
Avez-vous utiliser read.xls ?

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace. You can use it for several things:

# 2. Pre-load packages, so that users don't have to do this manually.
library(readxl)

# 1. Preload a dataset. The code below will read the csv that is stored at the URL's location.
# The movies variable will be available in the user's console.
urls <-  read.csv("crawl-scifi.csv", header = TRUE, sep=";")

```

*** =sct
```{r}
# The sct section defines the Submission Correctness Tests (SCTs) used to
# evaluate the student's response. All functions used here are defined in the 
# testwhat R package

msg_bad <- "That is not correct!"
msg_success <- "Exactly! There seems to be a very bad action movie in the dataset."

# Use test_mc() to grade multiple choice exercises. 
# Pass the correct option (Action, option 2 in the instructions) to correct.
# Pass the feedback messages, both positive and negative, to feedback_msgs in the appropriate order.
test_mc(correct = 2, feedback_msgs = c(msg_bad, msg_success, msg_bad, msg_bad)) 
```

--- type:NormalExercise lang:r xp:200 skills:1 key:2393503932
## Performance

In the previous exercise, you saw a dataset about movies. In this exercise, we'll have a look at yet another dataset about movies!

A dataset with a selection of movies, `movie_selection`, is available in the workspace.

*** =instructions
- Check out the structure of `urls`

*** =hint
- Use `str()` for the first instruction.


*** =pre_exercise_code
```{r}
# Pre-load a package in the workspace

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

# Test whether the student correctly used plot()
# Again, we use the automatically generated feedback here
test_function("plot", args = "x")
test_function("plot", args = "y")
test_function("plot", args = "col")

# Alternativeley, you can use test_function() like this
# test_function("plot", args = c("x", "y", "col"))

# It's always smart to include the following line of code at the end of your SCTs
# It will check whether executing the student's code resulted in an error, 
# and if so, will cause the exercise to fail
test_error()

# Final message the student will see upon completing the exercise
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:2393503932
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

