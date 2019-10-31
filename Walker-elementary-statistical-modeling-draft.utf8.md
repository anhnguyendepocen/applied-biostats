--- 
title: "Elementary Statistical Modeling for Applied Biostatistics"
author: "Copyright 2018 Jeffrey A. Walker"
date: "Draft: 2019-10-27"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: 
description: "A first course in statistical modeling for biology students"
---



# Preface {-}
*More cynically, one could also well ask "Why has medicine not adopted frequentist inference, even though everyone presents P-values and hypothesis tests?" My answer is: Because frequentist inference, like Bayesian inference, is not taught. Instead everyone gets taught a misleading pseudo-frequentism: a set of rituals and misinterpretations caricaturing frequentist inference, leading to all kinds of misunderstandings.* -- Sander Greenland

We use statistics to learn from data with uncertainty. Traditional introductory textbooks in biostatistics implicitly or explicitly train students and researchers to "discover by p-value" using hypothesis tests (Chapter \@ref(p-values)). Over the course of many chapters, the student learns to use something like a look-up table or a dichotomous key to choose the correct "test" for the data at hand, compute a test statistic for their data, compute a $p$-value based on the test statistic, and compare the *p*-value to 0.05. Textbooks typically give very little guidance about what can be concluded if $p < 0.05$ or if $p > 0.05$, but many researchers conclude, incorrectly, they have "discovered" something or "shown" an effect if $p < 0.05$ but found "no effect" if $p > 0.05$.

Researchers learn nothing useful from a hypothesis test -- that is, comparing $p$ to 0.05 (or some other arbitrary value). A $p$-value is a measure of compatibility between the data and the null hypothesis and, consequently, a pretty good, but imperfect tool to dampen the frequency that we are fooled by randomness. But if we are investigating the effects of an increasingly acidified ocean on coral growth, $p=0.002$ may be evidence of an effect of the experimental intervention, but, from everything we know about pH and cell biology, it would be absurd to conclude from any data that pH does not affect growth. To build useful models of how biological systems work, we want to know the magnitude of effects and our uncertainty in estimating these magnitudes. We can use a magnitude and uncertainty to make predictions about the future of coral reefs, under different scenarios of ocean acidification. We can use the estimated effects and uncertainty to model the consequences of the effects of acidification on coral growth on fish production or carbon cycling.

This book is an introduction to the estimation of effects of biological data, and measures of the uncertainty of theses estimates, using a statistical modeling approach. As an introduction, the focus will be linear models and extensions of the linear models including linear mixed models and generalized linear models. Linear models are the engine behind many hypothesis tests but the emphasis in statistical modeling is estimation and uncertainty instead of test statistics and $p$-values. All linear models, and their generalizations, are variations of

\begin{align}
y_i &\sim N(\mu_i, \theta)\\
\mathrm{E}(Y|X) &= \mu\\
\mu_i &= f(\beta_0 + \beta_1 x_i)
\end{align}

Chapter 1 explains the meaning of this **model specification** but the point to make here is that because all linear models and their generalizations are variations of this specification, a modeling strategy of learning or doing statistics is more coherent than the NHST strategy using look-up tables or dichotomous keys of hypothesis tests. Generalizations of the basic linear model include linear mixed models, generalized linear models, generalized additive models, causal graphical models, multivariate models, and machine learning. This book is not a comprehensive source for any of these methods but, instead, *a path of the critical elements leading you to the doorway to the vast universe of each of these methods*.

<div style="background-color:#cccccc; text-align:left; vertical-align: middle; padding:20px 47px;">
**NHST Blues** -- The "discovery by p-value" strategy, or Null-Hypothesis Significance Testing (NHST), has been criticized by statisticians for many, many decades. Nevertheless, introductory biostatistics textbooks written by both biologists and statisticians continue to organize textbooks around a collection of hypothesis tests, with much less emphasis on estimation and uncertainty. The NHST strategy of learning or doing statistics is easy in that it requires little understanding of the statistical model underneath the tests and its assumptions, limitations, and behavior. The NHST strategy in combination with point-and-click software enables "mindless statistics"^[Gegenrezer] and encourages the belief that statistics is a tool like a word processor is a tool, afterall, a rigorous analysis of one's data requires little more than getting p-values and creating bar plots. Indeed, many PhD programs in the biosciences require no statistics coursework and the only training available to students is from the other graduate students and postdocs in the lab. As a consequence, the biological sciences literature is filled with error bars that imply data with negative values and p-values that have little relationship to the probability of the data under the null. More importantly for science, the reported statistics are often not doing for the study what the researchers and journal editors think they are doing.
</div> 

## Math


## R and programming






<!--chapter:end:index.Rmd-->


# Part I: R fundamentals {-}

Placeholder


## Importing Packages
## Create an R Studio Project for this Class
## R Notebooks
### Create an R Notebook for this Chapter
### Create a "load-packages" chunk
### Create a "simple plot" chunk
### Create more R chunks and explore options and play with R code

<!--chapter:end:chapters/04-setup.Rmd-->


# Data -- Importing and Saving Data

Placeholder


## Create new notebook for this chapter
## Importing Data
### Excel File
#### Troubleshooting File Import
#### Peak at the imported data.table to check that the file was imported correctly and to learn about the contents.
#### Best practices for creating data files
#### Explore with plots
### Text File
## Reshaping Data
### Wide to long
### Stacking multiple sets of columns
## Miscellaneous data wrangling
### Vole data
## Saving Data
## Problems

<!--chapter:end:chapters/06-data-reading_writing.Rmd-->

# Part II: Some Fundamentals of Statistical Modeling {-}

<!--chapter:end:chapters/10-part-II-statistics-fundamentals.Rmd-->


# An Introduction to Statistical Modeling

Placeholder


## Two specifications of a linear model
### The "error draw" specification
### The "conditional draw" specification
### Comparing the two ways of specifying the linear model
## What do we call the $X$ and $Y$ variables?
## Statistical models are used for prediction, explanation, and description
## Modeling strategy
## A mean is the simplest model
## Assumptions for inference with a statistical model
## Specific assumptions for inference with a linear model
## "Statistical model" or "regression model"?
## GLM vs. GLM vs. GLS

<!--chapter:end:chapters/12-introduction-to-statistical-modeling.Rmd-->


# Variability and Uncertainty (Standard Deviations, Standard Errors, Confidence Intervals)

Placeholder


## The sample standard deviation vs. the standard error of the mean
### Sample standard deviation
### Standard error of the mean
## Using Google Sheets to generate fake data to explore the standard error
### Steps
## Using R to generate fake data to explore the standard error
### part I
### part II - means
### part III - how do SD and SE change as sample size (n) increases?
### Part IV -- Generating fake data with for-loops
## Bootstrapped standard errors
## Confidence Interval

<!--chapter:end:chapters/15-uncertainty_sd_and_se.Rmd-->


# Covariance and Correlation

Placeholder



<!--chapter:end:chapters/16-covariance-and-correlation.Rmd-->


# P-values

Placeholder


## $p$-values
## Creating a null distribution.
### the Null Distribution
### t-tests
### P-values from the perspective of permutation
## Statistical modeling instead of hypothesis testing
## frequentist probability and the interpretation of p-values
### Background
### This book covers frequentist approaches to statistical modeling and when a probability arises, such as the *p*-value of a test statistic, this will be a frequentist probability.
### Two interpretations of the *p*-value
#### Fisher's interpretation
#### Neyman-Pearson interpretation
### NHST
### Some major misconceptions of the $p$-value
#### Misconception: $p$ is the probability that the null is true *and* $1-p$ is probability that the alternative is true
#### Misconception: a $p$-value is repeatable
#### Misconception: 0.05 is the lifetime rate of false discoveries
#### Misconception: a low $p$-value indicates an important effect
#### Misconception: a low $p$-value indicates high model fit or high predictive capacity
##### What the $p$-value does not mean
### Recommendations
## Problems

<!--chapter:end:chapters/17-p-values.Rmd-->


# Creating Fake Data

Placeholder


### Continuous X (fake observational data)
### Categorical X (fake experimental data)
### Correlated X (fake observational data)
#### Generating correlated X variables
#### Creating mulitple X variables using the package mvtnorm
#### The rcov1 algorithm is naive
#### Generating multiple columns of X variables with a non-singular covariance matrix

<!--chapter:end:chapters/18-fake-data.Rmd-->

# Part III: Introduction to Linear Models  {-}

<!--chapter:end:chapters/20-part-iii-linear-model.Rmd-->


# A linear model with a single, continuous *X*

Placeholder


## A linear model with a single, continuous *X* is classical "regression"
### Using a linear model to estimate explanatory effects
#### Probabilistic vs. causal conditioning
### Using a linear model for prediction
### Reporting results
## Working in R
### Exploring the bivariate relationship between *Y* and *X*
### Fitting the linear model
### Getting to know the linear model: the `summary` function
### display: An alternative to summary
### Confidence intervals
### How good is our model?
### exploring a lm object
## Problems

<!--chapter:end:chapters/22-continuous_X.Rmd-->


# A linear model with a single, categorical *X*

Placeholder


## A linear model with a single, categorical *X* estimates the effects of *X* on the response.
### Table of model coefficients
### The linear model
#### Some math to convince you that the intercept of a linear model with a categorical $X$ is the mean of the reference group *and* the intercept of a line. And some math to convince you that the coefficient of a dummy variable in a linear model with a categorial $X$ is a difference in means *and* a slope.
### Reporting results
#### Harrell Plot of the data
#### In-text reporting
#### Correct interpretation of the Confidence Interval is key
## Comparing the results of a linear model to classical hypothesis tests
### t-tests are special cases of a linear model
#### Student's t-test
#### Welch's t-test
#### Paired t-test
### ANOVA is a special case of a linear model
## Working in R
### Fitting the model
### Changing the reference level
### An introduction to contrasts
### Harrell plot
#### Installing the harrellplot package
#### Using harrellplot to make a nice, publishable plot of treatment effects

<!--chapter:end:chapters/24-categorical_X.Rmd-->


# Model Checking

Placeholder


## Do coefficients make numeric sense?
## All statistical analyses should be followed by model checking 
## Linear model assumptions
## Diagnostic plots use the residuals from the model fit
### Residuals
### A Normal Q-Q plot is used to check normality
#### Right skewed
#### Excess zeroes
#### Constrained lower and upper bounds
#### Binary responses
### Outliers - an outlier is a point that is highly unexpected given the modeled distribution.
## Model checking homoskedasticity
## Model checking independence - hapiness adverse example.
## Using R

<!--chapter:end:chapters/26-model-checking.Rmd-->


# Model Fitting  and Model Fit (OLS)

Placeholder


## Least Squares Estimation and the Decomposition of Variance
## OLS regression
## How well does the model fit the data? $R^2$ and "variance explained"

<!--chapter:end:chapters/28-model-fit.Rmd-->


# Plotting Models

Placeholder


## Pretty good plots show the model and the data
### Pretty good plot component 1: Modeled effects plot
### Pretty good plot component 2: Modeled mean and CI plot with jittered raw data
### Combining Effects and Modeled mean and CI plots -- an Effects and response plot.
## Some comments on plot components
## Working in R
### Unpooled SE bars and confidence intervals
### Adding bootstrap intervals
### Adding modeled error intervals
#### Modeled error intervals of the effect
#### Modeled error intervals of the mean
#### Combining effects and response plots
### Adding p-values
### Adding custom p-values
### Plotting two factors
#### Three factors

<!--chapter:end:chapters/29-plotting_models.Rmd-->

# Part IV: More than one $X$ -- Multivariable Models {-}

<!--chapter:end:chapters/30-part-iv-multivariable.Rmd-->


# Adding covariates to a linear model

Placeholder


## Adding covariates can increases the precision of the effect of interest
### Interaction effects with covariates
### Add only covariates that were measured before peaking at the data
## Regression to the mean
### Do not use percent change, believing that percents account for effects of initial weights
### Do not "test for balance" of baseline measures

<!--chapter:end:chapters/32-covariates.Rmd-->


# Two (or more) Categorical $X$ -- Factorial designs

Placeholder


## Factorial experiments 
### Model coefficients: an interaction effect is what is leftover after adding the treatment effects to the control
### What is the biological meaning of an interaction effect?
### What about models with more than two factors?
### The additive model
### Contrasts -- simple vs. main effects
## Reporting results
### Text results
### Harrellplot
### Interaction plots
## Recommendations
## Working in R
## Problems

<!--chapter:end:chapters/34-factorial.Rmd-->


# ANOVA Tables

Placeholder


## Summary of usage
## Example: a one-way ANOVA using the vole data
## Example: a two-way ANOVA using the urchin data
### How to read an ANOVA table
#### Each row in the table tests a null hypothesis
#### What to do after ANOVA?
### How to read ANOVA results reported in the text
### Better practice -- estimates and their uncertainty
## Unbalanced designs
### What is going on in unbalanced ANOVA? -- Type I, II, III sum of squares
### Back to interpretation of main effects
### The anova tables for Type I, II, and III sum of squares are the same if the design is balanced.
## Working in R
### Type I sum of squares in R
### Type II and III Sum of Squares

<!--chapter:end:chapters/42-anova.Rmd-->


# Predictive Models

Placeholder


## Overfitting
## Model building vs. Variable selection vs. Model selection
### Stepwise regression
### Cross-validation
### Penalization
#### AIC
#### LASSO
## Shrinkage

<!--chapter:end:chapters/46-predictive-models.Rmd-->

# Part V: Expanding the Linear Model -- Generalized Linear Models and Multilevel (Linear Mixed) Models {-}

<!--chapter:end:chapters/50-part-v-expanding-linear-model.Rmd-->


# Generalized linear models I: Count data

Placeholder


## The generalized linear model
## Count data example -- number of trematode worm larvae in eyes of threespine stickleback fish
### Modeling strategy
### Checking the model I -- a Normal Q-Q plot
### Checking the model II -- scale-location plot for checking homoskedasticity
### Two distributions for count data -- Poisson and Negative Binomial
### Fitting a GLM with a Poisson distribution to the worm data
### Model checking fits to count data
#### Model checking a GLM I -- the quantile residual Q-Q plot
#### Model checking a GLM II -- a dispersion plot
### Fitting a GLM with a Negative Binomial distribution to the worm data
#### Model checking
#### Model means and coefficients
## Working in R
## Problems

<!--chapter:end:chapters/52-glm01-counts.Rmd-->


# Linear mixed models

Placeholder


## Random effects
## Random effects in statistical models
## Linear mixed models are flexible
## Visualizing block effects
## Linear mixed models can increase precision of point estimates
## Linear mixed models are used to avoid pseudoreplication
## Linear mixed models shrink coefficients by partial pooling
## Working in R
### coral data

<!--chapter:end:chapters/60-lmm01-blocking.Rmd-->


# Appendix 1: Getting Started with R {-}

Placeholder


## Get your computer ready
### Install R
### Install R Studio
### Resources for installing R and R Studio
### Install LaTeX
## Start learning
### Start with Data Camp Introduction to R
### Then Move to Introduction to R Studio
### Develop your project with an R Studio Notebook
## Getting Data into R
## Additional R learning resources
## Packages used extensively in this text

<!--chapter:end:chapters/92-R_resources.Rmd-->

# Appendix 2: Online Resources for Getting Started with Statistical Modeling in R {-}

Roughly, in order from most elementary to most advanced

[Learning Statistics with R](https://https://learningstatisticswithr-bookdown.netlify.com) by Danielle Navarro and adapted to Bookdown (for web viewing) by Emily Kothe.

[Statististical Thinking for the 21st Century](http://statsthinking21.org) by Russell A. Poldrack

[Regression Models for Data Science in R](https://leanpub.com/regmods) by Brian Caffo

[Broadening Your Statistical Horizons: Generalized Linear Models and Multilevel Models by J. Legler and P. Roback](https://bookdown.org/roback/bookdown-bysh/)

[Modern Statistics for Modern Biology](https://www.huber.embl.de/msmb/index.html)

[The Art of Data Science by Roger D. Peng and Elizabeth Matsui](https://bookdown.org/rdpeng/artofdatascience/)

<!--chapter:end:chapters/93-Getting_started_with_linear_modeling.Rmd-->
