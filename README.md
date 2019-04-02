# Cookiecutter For Neural Data Analysis

_A barebones and flexible project structure for neural data analysis._

#### [Project homepage](http://alexhwilliams.info/cookiecutter-neural-data/)

This project template was modified from [cookiecutter-data-science](http://drivendata.github.io/cookiecutter-data-science/), which is more full-featured and domain-agnostic.


### Requirements to use the cookiecutter template:
-----------
 - Python 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/ahwillia/cookiecutter-neural-data


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```
    ├── README.md          <- The top-level README that appears on Github.
    │
    ├── data               <- Folder containing all data.
    │   │
    │   ├── raw            <- Sub-folder containing immutable raw data.
    │   │
    │   └── processed      <- Processed data in a standardized format folder structure.
    │       │   │
    │       │   └─ metadata.yml    <- Specifies metadata shared across all subjects.
    │       │
    │       ├── subject_1
    │       │    ├── metadata.yml    <- Specifies metadata specific to subject 1.
    │       │    │
    │       │    ├── session_1
    │       │    │   ├── spikes.csv      <- Multi-unit or spike sorted data.
    │       │    │   ├── traces.csv      <- All analog signals (e.g. Ca imaging, behavior tracking).
    │       │    │   ├── events.csv      <- Times for stimuli, rewards, response times.
    │       │    │   └── metadata.yml    <- Specifies metadata specific to session 1, subject 1.
    │       │    │
    │       │    ├── session_2
    │       │    ⋮
    │       │    
    │       ├── subject_2
    │       ⋮
    │
    ├── {{cookiecutter.project_name}}   <- Source code for use in this project.
    │   │
    │   ├── __init__.py      <- Makes src a Python module
    │   ├── data.py          <- Scripts to generate, download, or transform data.
    │   ├── models.py        <- Scripts for training models, or using them for prediction.
    │   ├── visualize.py     <- Scripts to create exploratory and results oriented visualizations
    │   ⋮
    │
    ├── results            <- Folder containing model parameters, model predictions, etc.
    │
    ├── notebooks          <- Jupyter notebooks for exploratory analyses.
    │
    ├── reports
    │   ├── notes          <- Technical notes and citations.
    │   ├── paper          <- Final publication.
    │   └── figures        <- Scripts for generating each final figure.
    │
    ├── requirements.txt   <- Lists required python libraries.
    ├── setup.py           <- makes project installable (`python setup.py develop`) or (`pip install -e .`)
    ├── .gitignore         <- Specifies files for git to ignore (e.g. large data files)
    └── LICENSE            <- LICENSE file if you plan to make your code open source.
```
