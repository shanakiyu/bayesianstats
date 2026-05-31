# Bayesian Analysis: UFO Sightings and Hollywood Influence

## Project Overview
This project investigates a sociological and cognitive phenomenon: Does the release of major Hollywood science-fiction blockbusters statistically increase the rate of reported UFO sightings in the United States? Rather than treating UFOs as physical anomalies, we approach them as measurable traces of human attention and media exposure. Using a Bayesian statistical framework, we analyzed decades of UFO reports alongside movie release data to test for a cultural "priming effect."

## Team
* Emna Ben Ameur
* Lélie Chenouga
* Safia Lamri
* Nina Vivier Barte

## Team Contributions & Workflow
* Emna Ben Ameur and Nina Vivier Barte: Led the technical and data engineering efforts. This included API data extraction, dataset cleaning, and coding the Bayesian Gamma-Poisson model in Python.
* Lélie Chenouga and Safia Lamri: Led the analytical and academic efforts. This included analyzing the statistical outputs, conducting historical and bibliographic research, and authoring the final academic report.
* Note on Git History: The coding and data exploration were conducted collaboratively using Google Colab. Consequently, the commit history on this repository does not fully reflect individual contributions, as the final notebooks were pushed to GitHub by a single account after the collaborative work was completed.

## Data Sources
1. UFO Sightings: Sourced from the National UFO Reporting Center (NUFORC) via Kaggle. The dataset was rigorously cleaned, filtering for US-only sightings, realistic durations (1 sec to 24h), and dates post-1990 to align with the modern blockbuster era and internet reporting.
2. Hollywood Sci-Fi Movies: Extracted using the TMDB API. We filtered the database to keep only major cultural events (movies with > 1,000 votes) to ensure the films studied had massive public visibility.

## Methodology
We modeled the daily UFO sighting counts as a rare stochastic event using a Poisson process. To test our hypothesis, we applied Bayesian Inference via the Gamma-Poisson conjugate model:
* Prior: The baseline sighting rate in the 30 days before the movie release (modeled with a Gamma distribution).
* Posterior: The updated rate in the 30 days after the movie release, updated analytically.
* Evaluation: We used Monte Carlo simulations (100,000 draws) to calculate the probability of a rate increase.

## Key Results
* Global Impact: Across the 335 blockbusters analyzed, the pooled data shows a definitive rightward shift in the posterior distributions.
* Conclusion: We reject the null hypothesis (H0). The data strongly supports our alternative hypothesis (H1): Hollywood sci-fi films act as a powerful cognitive prior. By saturating the media space, they temporarily configure public perception, making people more likely to interpret and report ambiguous aerial stimuli as UFOs.

## Repository Structure
* BayesianProject_UFO_SFMovies.ipynb: The main Jupyter Notebook containing the data pipeline, Bayesian modeling, and data visualization.
* scrubbed.csv: The raw NUFORC UFO dataset.
* hollywood_scifi_movies_INTEGRAL.csv: The TMDB movie dataset.
* Bayesian_project.pdf: The detailed academic report explaining the historical context, methodology, and epistemological conclusions.
* PROJECT.ipynb: The notebook used to scrap the TMDB movie dataset with the TMDB API.

## How to Run the Code
This project is optimized for Google Colab.
1. Open BayesianProject_UFO_SFMovies.ipynb in Google Colab or your local Jupyter environment.
2. Run the Data Import cell.
3. When prompted, upload the two CSV datasets (scrubbed.csv and hollywood_scifi_movies_INTEGRAL.csv).
4. Execute the rest of the notebook sequentially to reproduce the data cleaning, time-window generation, Bayesian inference, and global posterior plots.

## Acknowledgments & Tools
* **AI Assistance:** Large Language Models (LLMs) were used strictly as coding assistants (for code formatting, minor debugging, and translating text to English). The conceptual framework, dataset selection, Bayesian modeling, and epistemological conclusions are entirely the original work of the authors.
