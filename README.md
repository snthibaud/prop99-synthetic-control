# Proposition 99: a synthetic control replication

This repository is a replication and stress test of the synthetic control analysis in [Abadie, Diamond and Hainmueller (2010)](https://doi.org/10.1198/jasa.2009.ap08746) (ADH). The notebook fits the simplest version of the method: donor weights are chosen by least squares to match California's 1970-1988 cigarette sales, with no predictors. The headline results are close to the paper's. The average gap for 1989-2000 is -19.5 packs per capita, and ADH's published weights on the same data give -19.0. Placebo p-values run from 0.031 to 0.179 depending on the test statistic. The notebook was executed before committing, so the outputs and charts can be read directly on GitHub.

## Run it

```bash
uv sync
uv run --with jupyterlab jupyter lab prop99_synthetic_control.ipynb
```

## Data

The data are per-capita cigarette sales for 39 states, 1970-2000, from the synthdid R package (synth-inference/synthdid on GitHub), copyright 2019 Stanford University, BSD-3-Clause licence. The file is unchanged and the licence text is included in data/LICENSE-synthdid.txt.
