<h1>Bayesian Analysis of UFO Sightings and Hollywood Influence</h1>

<h2>Project Overview</h2>

<p>
This project investigates whether the release of major science-fiction films influences the frequency of reported UFO sightings.
</p>

<p>
We model UFO sightings as rare stochastic events and use Bayesian inference to evaluate whether their rate increases following the release of selected films.
</p>

---

<h2>Conceptual Framework</h2>

<ul>
  <li>UFO sightings are modeled as random events over time.</li>
  <li>A baseline rate is estimated using a Poisson distribution.</li>
  <li>Bayesian inference updates this rate after new observations.</li>
</ul>

---

<h2>Methodology</h2>

<h3>Statistical Model</h3>

<p>
We model sightings using a Poisson process with parameter λ (rate of occurrence).
Bayesian inference allows us to update λ given observed data:
</p>

<pre>
P(λ | data) = P(data | λ) × P(λ) / P(data)
</pre>

<h3>Hypotheses</h3>

<ul>
  <li><strong>H0:</strong> The rate of UFO sightings remains constant.</li>
  <li><strong>H1:</strong> The rate increases after the release of a science-fiction film.</li>
</ul>

---

<h2>Data Sources</h2>

<ul>
  <li>
    <strong>UFO Sightings Dataset</strong><br>
    Source: NUFORC (via Kaggle)<br>
    Historical records of UFO sightings.
  </li>
  <br>
  <li>
    <strong>Movie Release Dates</strong><br>
    Selected science-fiction films (e.g. Independence Day, Arrival, Contact, Signs)<br>
    Collected via TMDB.
  </li>
</ul>

---

<h2>Project Structure</h2>

<pre>
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
</pre>

---

<h2>Workflow</h2>

<ol>
  <li>
    <strong>Data preprocessing</strong>
    <ul>
      <li>Convert dates to datetime format</li>
      <li>Clean and filter observations</li>
    </ul>
  </li>

  <li>
    <strong>Time window construction</strong>
    <ul>
      <li>Define 3-month periods before and after each film release</li>
    </ul>
  </li>

  <li>
    <strong>Statistical analysis</strong>
    <ul>
      <li>Estimate baseline λ</li>
      <li>Apply Bayesian updating</li>
    </ul>
  </li>

  <li>
    <strong>Visualization</strong>
    <ul>
      <li>Generate comparative plots</li>
      <li>Produce summary tables</li>
    </ul>
  </li>
</ol>

---

<h2>Expected Outputs</h2>

<ul>
  <li>Time series plots of UFO sightings</li>
  <li>Comparison of rates before and after film releases</li>
  <li>Posterior distribution summaries</li>
</ul>

---

<h2>Epistemological Perspective</h2>

<p>
This project raises the question of whether UFO sightings reflect physical phenomena or sociocultural dynamics influenced by media and collective perception.
</p>

---

<h2>Team</h2>

<ul>
  <li>Emna Ben Ameur</li>
  <li>Safia Lamri</li>
  <li>Lélie Chenouga</li>
  <li>Nina Vivier-Barte</li>
</ul>

---

<h2>Current Status</h2>

<p>
The repository currently contains only the original datasets.
</p>

<p>
Next steps:
</p>

<ul>
  <li>Data preprocessing</li>
  <li>Implementation of the statistical model</li>
  <li>Visualization and interpretation</li>
</ul>

---
