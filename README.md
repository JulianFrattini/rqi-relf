# Relevant Factors of Requirements Quality: Replication Package

[![GitHub](https://img.shields.io/github/license/JulianFrattini/rqi-relf)](./LICENSE)

This repository contains the replication package for the case study on identifying relevant factors of requirements quality. In this study, we used the requirements quality theory \[1\] as a frame to identify which quality and context factors \[2\] are relevant to the specific company case. This repository contains the (anonymized) data sets, scripts to analyze them, and figures to visualize them.

## Contributors Information

| Name                         | Affiliation                              | Email                             |
| ---------------------------- | ---------------------------------------- | --------------------------------- |
| Julian Frattini              | Blekinge Institute of Technology, Sweden | julian.frattini@bth.se            |

## Description of the Artifacts

This repository contains the following artifacts:

* *data/* : folder for all data-related information
  * [columns.json](./data/columns.json) : List of relevant columns and available values per column
* *doc/* : folder containing all additional documentation and supplementary material
  * [Interview Coding Guideline](./doc/Interview%20Coding%20Guideline.pdf) : guideline for coding the interview transcripts
* *figures/* : folder for all figures
  * *graphml/* : figures in editable `.graphml` format
    * *activity-model.graphml* : tree of activities and attributes
    * *interaction-example.graphml* : mapping a statement describing an interaction effect to the requirements quality theory
    * *method-visualization.graphml* : visual overview of the data collection and analysis method
    * *requirements-quality-theory.graphml* : simplified version of the requirements quality theory \[1\]
  * *pdf/* : the same figures but in viewable `.pdf` format
* *src/* : folder containing all source code
  * *analytics/* : folder for all source code related to analysis
    * [evaluation.ipynb](./src/analytics/evaluation.ipynb) : notebook to filter and aggregate the data to themes
    * [interrater-agreement](./src/analytics/interrater-agreement.ipynb) : notebook to calculate the agreement between two independent raters coding the interview data
  * [exploration.ipynb](./src/exploration.ipynb) : notebook to further explore the data set
  * [requirements.txt](./src/requirements.txt) : list of python libraries required to execute the source code

The artifact does not contain verbatim interview or issue report data due to privacy reasons.

## System Requirements

The following requirements must be met in order to utilize the artifacts contained in this repository:

* To utilize **the data**, you need a spreadsheet software like Microsoft Excel to open the .xlsx file.
* To exectute **the code**, [Python 3.10](https://www.python.org/downloads/release/python-3100/) must be available and an editor software like [Visual Studio Code](https://code.visualstudio.com/download) is recommended.
* To edit **the figures**, you require an editor capable of opening Graph Markup Language (`.graphml`) files, for example the [yEd Graph Editor](https://www.yworks.com/products/yed).

## Installation Instructions

To execute the code contained in this repository, make sure all requirements contained in the [requirements.txt](./src/requirements.txt) are installed by executing `pip install -r requirements.txt`. To avoid conflicts with the local Python environment, create a separate [virtual environment](https://docs.python.org/3/library/venv.html):

1. Create a virtual environment with `python -m venv .venv`
2. Activate the virtual environment with `./venv/Scripts/activate`
3. Install the requirements as described above.
4. Install the ipykernel either by selecting the virtual environment `.venv` as the runtime environment for the Jupyter notebook in VS Code (which will trigger VS Code to automatically install the ipykernel) or [install it manually](https://github.com/ipython/ipykernel).

Once the virtual environment is running and all requirements installed and ipykernel are installed, the Jupyter notebook can be executed from the virtual environment.

## Steps to Reproduce

Execute the code blocks of the following Jupyter notebooks from top to bottom to reproduce the results from the manuscript:

- [interrateragreement.ipynb](./src/analytics/interrater-agreement.ipynb): calculation of the inter-rater agreement between the author and the independent rater
- [evaluation.ipynb](./src/analytics/evaluation.ipynb): filtering of the raw data and aggregation of the data into larger, more meaningful units

Additionally, you can use the file [exploration.ipynb](./src/exploration.ipynb) to explore the data further and in more depth.

## References

\[1\] Frattini, J., Montgomery, L., Fischbach, J., Mendez, D., Fucci, D., & Unterkalmsteiner, M. (2023). Requirements quality research: a harmonized theory, evaluation, and roadmap. Requirements Engineering, 1-14. https://doi.org/10.1007/s00766-023-00405-y

\[2\] Femmer, H., Mund, J., & Fernández, D. M. (2015, May). It's the activities, stupid! a new perspective on RE quality. In 2015 IEEE/ACM 2nd International Workshop on Requirements Engineering and Testing (pp. 13-19). IEEE. https://doi.org/10.1109/RE54965.2022.00041

## Licensing

Copyright © 2023 Julian Frattini. This work is licensed under [MIT License](./LICENSE).