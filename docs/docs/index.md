# Cookiecutter Data Science

_A barebones template for neural data analysis._

<span style="color:red">**Note:** this cookiecutter template is a work in progress.</span>

## Why use this project structure?

See [**cookiecutter-data-science**](https://drivendata.github.io/cookiecutter-data-science/) and references/links therein for why thinking about project organization is important. This project template was adapted for neuroscience applications. In particular, this template *sets a standard folder/directory structure for multi-subject data*.

### Requirements

 - Python 3.5+
 - [cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: `pip install cookiecutter`


### Starting a new project

Starting a new project is as easy as running this command at the command line. No need to create a directory first, the cookiecutter will do it for you.

```nohighlight
cookiecutter https://github.com/ahwillia/cookiecutter-neural-data
```

## Directory structure

```nohighlight
    ├── README.md          <- The top-level README that appears on Github.
    │
    ├── data               <- Folder containing all data.
    │   │
    │   ├── raw            <- Sub-folder containing immutable raw data.
    │   │
    │   └── processed      <- Processed data in a standardized format folder structure.
    │       │   
    │       ├── metadata.yml    <- Specifies metadata shared across all subjects.
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
    ├── setup.py           <- makes project installable (`python setup.py develop`)
    ├── .gitignore         <- Specifies files for git to ignore (e.g. large data files)
    └── LICENSE            <- LICENSE file if you plan to make your code open source.
```

## Related Projects

Ultimately, this project template will (hopefully) be integrated with other tools like [`neuroglia`](https://github.com/AllenInstitute/neuroglia).
