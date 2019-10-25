# Data-Report-Generator

This R Markdown documents automatically generates a report for a given dataset.

It takes as input:
 - df: the dataframe we want to analyse
 - max_nb_distinct_hist: a threshold for the maximum number of distinct values for categorical variables for which we plot a histogram of counts. This avoids overplotting in cases where a categorical has many distinct values.
 - min_cor_to_draw: a threshold for the minimal correlation between two numerical variables for us to draw their scatterplot. This should be set to 0 to draw all scatterplots.
 
# Usage 

> rmarkdown::render("data_report_generator.Rmd",params = list(df = mtcars, max_nb_distinct_hist = 10, min_cor_to_draw = 0.4), output_file = "myoutput.html")