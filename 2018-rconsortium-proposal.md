---
title: "A unified platform for missing values methods and workflows"
date: "2018-03-27"
output:
  html_document:
    keep_md: yes
bibliography: proposal.bib
---

_Applicants_

_Julie Josse, Ecole Polytechnique, France; julie.josse@polytechnique.edu_

_Nicholas Tierney, Monash university, Australia; nicholas.tierney@monash.edu_

## The Problem

Missing values are an unavoidable problem when working with real world
data. They occur for many reasons. For example, individuals choose not
to answer survey questions, weather measurement devices fail in wet
weather, or participants drop out of a study. Missing values are
problematic, as most statistical models and visualisation methods
require complete data. This problem is exacerbated as more data from
different sources become available, which may not have been designed to
be analysed together. Missing values are a problem, so what do we do
about it?

There are many ways deal with missing data in an analysis.
The most common approach, despite decades of research advocating
otherwise, is too toss out cases with missing values. At best, this is
inefficient; it wastes information from the partially observed cases. At
worst, it results in biased estimates, particularly when the
distributions of the missing values are systematically different than
the observed values. Fortunately, there are better alternatives to
tossing out cases [@Schafer2002; @Little2002; @VanBuuren2012,
@Carpenter2012]. Some analysts use model-based
approaches, integrating likelihoods or posterior distributions over
missing values. Some use imputation, creating single or multiple
completed datasets. Some use weighting approaches, appealing to ideas
from the design-based literature in survey sampling.

R has many more approaches for working with missing data than other statistical
software. To be exact, there are currently 274 R
packages on CRAN that mention missing data or imputation in their DESCRIPTION
files. There are imputation packages such as mice, Amelia, and mi 
[@mi; @amelia; @mi]. There are providing descriptive statistics and 
visualisations, like naniar, VIM, and MissingDataGUI [@naniar; @VIM; @Cheng2015]. 
There are still many other packages developed to handle complex, heterogenous
(categorical, quantitative, ordinal variables) data of large dimension 
multi-level data, such as missMDA, and MixedDataImpute 
[@Josse2016; @Murray2015].

There are many missing data packages in R that solve real problems. A
problem with so many options is navigating the decision paralysis of
choice - which one is right for the case at hand. It is not trivial.

This application aims to valorize current work in missing data by
providing a unified platform that lists and organizes existing packages,
articles, tutorials, documentation, and workflows for analyses with
missing data. The platform will be easy to extend, and will be well
documented, so it can easily incorporate future research in missing
values. It will also have a focus on fostering a welcoming community.

We hope that such a tool will enable R to consolidate and strengthen its
leadership position on the subject.

## The Plan

To create this platform, we wish to address the objectives in four parts.

**Part one: listing available R packages**

We will list available packages for working with missing data, with a
brief description. These can be used as a task-view on the subject, as
there is currently no task view specific to missing data, aside from
sections social sciences
([*https://cran.r-project.org/web/views/SocialSciences.html*](https://cran.r-project.org/web/views/SocialSciences.html))
and Multivariate Statistics
([*https://cran.r-project.org/web/views/Multivariate.html*](https://cran.r-project.org/web/views/Multivariate.html)).
We intend to make a call out to other package authors and research in
missing data in the R community to join this platform. One person we
intend to contact is Stefan van Buuren, whose website
[*http://www.stefvanbuuren.nl/mi/Software.html*](http://www.stefvanbuuren.nl/mi/Software.html)
is also often used as a reference.

**Part two: list articles and related works by theme**

Similar to part one with R packages, we will list articles and related
works, organising by theme. This can be rather laborious work, to ensure
robustness we will also put a call out for authors to submit their
articles or works to be reviewed for placement on the platform/website.

**Part three: Tutorials and workflows.**

In part three, we provide peer reviewed tutorials and analysis workflows
with a variety of different kinds of missing data. For example, these
could focus on exploration and visualization at different stages of the
analyses, advantages and drawbacks of methods such as likelihood based
approaches, and imputation methods. After imputation or other treatment
of the missing data, we will encourage assessing the impact on
subsequent analyses and inferences.

**Part four: future extensions and beyond**

By providing a platform and community to discuss missing data in R,
software, and approaches and workflows, we are providing a base from
which we can grow. For example, this platform could collect datasets to
benchmark imputation methods, which are currently not being done
anywhere in the world. By having a community involved in this, we can
then have useful discussion on the benchmarks, even organize events like
a challenge to provide the best imputation methods, in a similar fashion
to the M4 forecasting competition
(https://robjhyndman.com/hyndsight/m4comp/).

Other ideas that we would like to consider are describing universal
approaches to multiple imputation, other special types of missing value
(other than NA like STATAs special missing values), altering messages in
the base R to encourage other approaches than deleting missing
observations by default, or at least indicating the risks, etc.

Expected impact: Missing values handling is crucial for data analysis
and an easy to use platform could allow users to give more values to
their analyses.


## Team

[Julie Josse](http://juliejosse.com/) is Professor of Statistics at Ecole
Polytechnique in France. Julie was trained as an engineer in statistics in an
Agronomy University. Her PhD was given the award "Best PhD in Applied Statistics" by the French Statistical Society. She has specialized
in missing data, visualization and the nonparametric analyses of complex data
structures. Her work was rewarded by a European Union grant in 2013 to increase
her research potential and to spend a year at Stanford University. She has
published over 30 articles and written 2 books in applied statistics. Her
vocation is to push methodological innovation to bring useful application of her
research to users, in particular in bio- and food science. Julie Josse has
developed packages to transfer her works such as missMDA dedicated to missing
values. Her experience on dealing with incomplete data is recognized by the
community: she has just compiled a "Statistical Science" special issue to have a
snapshot of the state of the art, she organized the first conference on missing
value, "MissData" in 2015 and she is often invited to give lectures around the
world to share her experience. She is deeply involved in the R community and is
part of Rforwards to widen the participation of minorities in the communities.

[Nicholas Tierney](http://www.njtierney.com/) has a PhD in statistics and is a research fellow in the department of econometrics and business statistics. Nick has written two R packages that 
focus on data visualisation and approaches for exploring missing data: visdat, 
and naniar. He has also authored a peer reviewed paper on model based approaches
for understanding structure in missing data. Nick is very involed with the R
community, having been the lead organiser for the first two Australian rOpenSci
ozunconferences ([2017](auunconf.ropensci.org) and [2018](ozunconf17.ropensci.org)), 
and presenting at R user groups in Brisbane and Melbourne in Australia, and The Bay Area
in California. In addition to his experience with statistics and R package development, Nick brings experience on wrangling groups of people together to build projects and comminities.

We will also contact contributors to missing data, such as François Husson, Professor of Statistics at Agrocampus Ouest, France, and Stefan van Buuren, and welcome other interest.

## Project Milestones

We would like to conduct the project over the following time periods (M1 refers
to month 1):

### Milestone one: listing available R packages

1. (M1-M3). Create the website infrastructure, so that it is easy to
navigate and to update.

### Milestone two: list articles and related works by theme

2. (M4-M6). List, organize the packages/articles available.

### Milestone three: Tutorials and workflows.

3. (M7-M10). Write documentation/tutorials to better reproduce the
existing studies and help the users with their own analyses. The idea is
to suggest some good practice pipelines to analyse data with missing
values. Some tutorials will be done with small videos.

### Milestone four: future extensions and beyond

4. (M11-M12). Organize data benchmark repository.

We would also at this point like to start considering ideas such as universal approaches to multiple imputation, implementing other special types of missing value (other than NA like STATAs special missing values), altering messages in the base R to encourage other approaches than deleting missing observations by default, or at least indicating the risks, etc.

## How ICS can help

## Funding

The following table details the cost items.

| Item                                                      | Cost      |
|:----------------------------------------------------------|-----------|
| Employ a research assistant for one year (10 hrs / week)  | Euro 7000 |
| Meeting with partners                                     | Euro 2500 |
| online materials                                          | Euro 500  |
| Total                                                     | Euro 10000|

### Employing research assistant(s)

Julie and Nick will jointly supervise a research assistant, who will help with the Milestones desribed.

### Meeting with Partners

It will be of great benefit to for both of us to work together face to face for one week or so. In this case it would either be a trip from France to Australia, or Australia to France. We'd like to request support for helping with the long haul flight.

### Online materials

These costs will cover a domain name server costs for us to set up an online community.

## Dissemination

The platform we create will serve as the primary dissemination of the project. We will also write blog posts for the R Consortium site, and Nick will also blog about the experience on his personal blog.

we can maybe speak about using social media, twitter, etc...
For the team, say that we are going to contact maybe van der loo, and others?

# References
