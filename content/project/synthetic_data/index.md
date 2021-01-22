---
date: "`r format(Sys.time(), '%d-%m-%Y')`"
external_link: ""
image:
  caption: Photo by Adobe Stock
  focal_point: Smart
# links:
# - icon: twitter
#   icon_pack: fab
#   name:
#   url:
slides:
summary: Synthetic data allows for openly sharing of research data, without disclosing identifying information of the participants, that could be as informative as the actually observed data.
tags:
- Multiple Imputation
title: Multiple Imputation of Synthetic Data
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
---

Publicly available research data could dramatically improve the scientific returns of research, given the same data collection effort. However, directly sharing the research data might harm the privacy and confidentiality of the participants. A solution has been proposed by Donald Rubin and Roderick Little, who, in two separate papers, have given rise to the procedure of creating *synthetic data*. Both scholars proposed to create multiple, synthetic versions of a dataset that is stripped of all possibly identifying information, by replacing this information by artificially created synthetic data that is unrelated to the persons in the data. Both approaches are build upon the foundation of multiple imputation for missing data, but rather than imputating the missing values, observed values are *overimputed* with multiple draws from the posterior predictive distribution of the observed data. 

If the imputation procedure is of sufficient quality, the synthetic datasets are almost equally informative as the observed data, without disclosing any identifying information. However, to make this work, creating synthetic data should be a cakewalk, as researchers collecting data can generally not be expected to be experts in this field. To ease the effort involved with creating missing data, together with [Gerko Vink](https://www.gerkovink.com/) and [Stef van Buuren](https://stefvanbuuren.name/), I am extending the R-package [MICE](https://amices.org/mice/), which is currently restricted to the imputation of missing data. Hereby, we aim at relieving the burden associated with generating synthetic data, while maintaining the data quality that is required to make valid inferences.


