# STAT 451 — Bayesian Statistics

R and Stan coursework, Monte Carlo methods, and hierarchical Bayesian logistic regression.

Coursework portfolio of **Han Sun ([shufubianyibo](https://github.com/shufubianyibo))**. This repository collects source snapshots from local projects so they can be browsed directly from my personal GitHub profile.

## Main project

### [Hierarchical Bayesian logistic regression](coursework/451projectHan.Rmd)

The project models a binary marital-status outcome using age, gender, urban residence, and education, together with province-level intercepts. The Stan model uses a non-centered hierarchical parameterization: province effects share a population mean and a learned scale, allowing information to be pooled across regions.

The R workflow prepares the design matrix and province identifiers, fits the model with `rstan`, and inspects posterior summaries, trace plots, and coefficient distributions. The notebook specifies four chains with 2,000 iterations each and a fixed random seed. These are model and sampling settings, rather than a claim about predictive performance or convergence on a new run.

**Start here:** [`451projectHan.Rmd`](coursework/451projectHan.Rmd). [`451project.Rmd`](coursework/451project.Rmd) is an alternate notebook with the same model structure. The raw `adult_2022.csv` dataset is not included in this public collection.

## Supporting coursework

The remaining [R notebooks](coursework/) cover posterior calculations, Monte Carlo estimation, and Bayesian model fitting. [`MCMC_beta_binomial.R`](coursework/MCMC_beta_binomial.R) and [`intro_Monte_Carlo.Rmd`](coursework/intro_Monte_Carlo.Rmd) are useful entry points for the simulation exercises. Course tutorials are retained as supporting material, with their original headers.

## All projects

| Project | Source files |
| --- | ---: |
| [coursework](coursework/) | 16 |

## Running the projects

Each directory is independent. Read its README, build file, tests, and `PORTFOLIO.md` before running. Original course infrastructure, data, or toolchains may be required. This publication checks source packaging; it does not certify that every historical project builds on a current machine.

## Attribution

These are individual and collaborative course projects. Course starter code, supplied tests, and third-party dependencies are included where needed. Original credits and licenses are retained. Each `PORTFOLIO.md` links to the source repository and records its base commit and commit authors when available. Source-file counts include tests and scaffolding and are not a measure of individually authored work. Snapshots were collected on 2026-11-17; original working directories were left unchanged.

## Data and dependencies

R notebooks use packages such as `rstan`, `dplyr`, and `ggplot2`; see their library calls for dependencies. The project notebooks fit a hierarchical logistic regression with province-level effects. Raw CSV datasets and rendered homework documents are not included. Supply the datasets named in each notebook from their authorized original source.
