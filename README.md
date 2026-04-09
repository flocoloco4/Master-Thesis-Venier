# The Geography of Token Efficiency in Large Language Models

This repository contains the data collection and analysis code for the master thesis
"The Geography of Token Efficiency in Large Language Models" by Florian Mathias Venier,
University of Vienna, 2026.

## Overview

This thesis examines token efficiency as a spatial construct by measuring how
efficiently three tokenizer architectures encode place names across a global H3
hexagonal grid. The analysis covers 6,911 H3 cells at resolution 3, using place
name data from OpenStreetMap and comparing the tokenizers of GPT-4o, DeepSeek-LLM-7B,
and Mistral-7B.

## Data Sources

| Dataset | Source | Year |
|---|---|---|
| Place names | OpenStreetMap via Overpass API | 2025 |
| Population grid | GHS Population Grid, EU Joint Research Centre | 2025 |
| Internet penetration | World Bank, indicator IT.NET.USER.ZS | 2022 |
| Carbon intensity | Our World in Data, sourced from Ember and IEA | 2022 |
| Country boundaries | Natural Earth 110m Admin 0 | 2024 |

## Requirements

pip install overpy h3 tiktoken transformers geopandas shapely
rasterio rasterstats pyproj libpysal esda scipy
pandas numpy matplotlib requests networkx

## Note on Reproducibility

The results produced by this code may not match the exact figures reported in the
master thesis in all cases. The analysis was conducted over an extended period and
involved multiple iterative steps, intermediate data transformations, and corrections
along the way. Some analytical steps were refined or rerun with updated parameters,
and not all intermediate states were preserved. The code in this repository reflects
the final cleaned version of the pipeline and produces results that are consistent
with the findings of the thesis, but minor numerical differences in some tables and
figures are possible. The spatial patterns, rank orderings, and statistical conclusions
reported in the thesis are robust and are reproduced correctly by this code.

## Citation

Venier, F. M. (2026). *The Geography of Token Efficiency in Large Language Models*.
Master thesis, University of Vienna.

## Supervisor

Krzysztof Janowicz, University of Vienna
