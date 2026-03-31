Bayesian Analysis of UFO Sightings and Hollywood Influence
Project Overview

This project investigates the following question:

Does the release of major science-fiction films influence the frequency of reported UFO sightings?

We approach this problem using Bayesian inference and a Poisson process, modeling UFO sightings as rare stochastic events whose rate may be affected by cultural phenomena such as cinema.

Conceptual Framework

UFO sightings are modeled as random events occurring over time. We assume a baseline rate of sightings and examine whether this rate changes after the release of selected science-fiction films.

The analysis relies on:

Poisson distribution for modeling rare events

Bayesian inference to update the rate parameter based on observed data

Methodology
Statistical Model

We model the number of sightings with a Poisson process parameterized by λ (rate of occurrence). Bayesian inference is used to update λ after observing new data.

P(λ | data) = P(data | λ) * P(λ) / P(data)

Hypotheses

H0 (null hypothesis): The rate of UFO sightings remains constant over time.

H1 (alternative hypothesis): The rate of UFO sightings increases after the release of a science-fiction film.

Data Sources

UFO Sightings dataset
Source: NUFORC (via Kaggle)
Contains historical records of reported UFO sightings.

Movie release dates
A selection of major science-fiction films (e.g. Independence Day, Arrival, Contact, Signs), collected via TMDB.

Project Structure
project/
│
├── data/
│   ├── ufo_sightings.csv
│   └── movies.csv
│
├── src/
│   └── analysis.py
│
├── outputs/
│   ├── plots/
│   └── tables/
│
└── README.md
Workflow

Data preprocessing

Convert date fields to datetime format

Clean and filter relevant observations

Time window construction

Define periods of 3 months before and after each film release

Statistical analysis

Estimate the baseline rate λ

Apply Bayesian updating for each time window

Visualization

Generate plots comparing pre- and post-release periods

Produce summary tables of results

Expected Outputs

Time series plots of UFO sightings

Comparison of estimated rates before and after film releases

Tables summarizing posterior distributions

Epistemological Perspective

This project also addresses a broader question: whether UFO sightings should be interpreted as observations of physical phenomena or as sociocultural constructs influenced by media and collective imagination.

Team

Nina Vivier-Barte

Emna Ben Ameur

Safia

Lelie

Current Status

The repository currently contains:

Raw datasets only

Next steps include:

Data preprocessing

Implementation of the statistical model

Generation of visualizations and interpretation of results
