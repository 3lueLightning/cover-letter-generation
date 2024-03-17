# cover-letter-generation

[![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v1.json)](https://github.com/charliermarsh/ruff)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## ✨ Features and Tools

Information about all the features and tools used in this project: <https://joserzapata.github.io/data-science-project-template/#features-and-tools>

Features                                     | Package  | Why?
 ---                                         | ---      | ---
Dependencies and env                         | [Poetry] | [article](https://mathdatasimplified.com/2023/06/12/poetry-a-better-way-to-manage-python-dependencies/)
Project configuration file                   | [Hydra]  |  [article](https://mathdatasimplified.com/2023/05/25/stop-hard-coding-in-a-data-science-project-use-configuration-files-instead/)
Lint - Format, sort imports  (Code Quality)  | [Ruff] | [article](https://www.sicara.fr/blog-technique/boost-code-quality-ruff-linter)
Static type checking                         | [Mypy] | [article](https://python.plainenglish.io/does-python-need-types-79753b88f521)
code security                                | [bandit] | [article](https://blog.bytehackr.in/secure-your-python-code-with-bandit)
Code quality & security each commit          | [pre-commit] | [article](https://dev.to/techishdeep/maximize-your-python-efficiency-with-pre-commit-a-complete-but-concise-guide-39a5)
Test code                                    | [Pytest] | [article](https://realpython.com/pytest-python-testing/)
Test coverage                                | [coverage.py] [codecov] | [article](https://martinxpn.medium.com/test-coverage-in-python-with-pytest-86-100-days-of-python-a3205c77296)
Project Template                             | [Cruft] or [Cookiecutter] | [article](https://medium.com/@bctello8/standardizing-dbt-projects-at-scale-with-cookiecutter-and-cruft-20acc4dc3f74)
Folder structure for data science projects   | [Data structure] | [article](https://towardsdatascience.com/the-importance-of-layered-thinking-in-data-engineering-a09f685edc71)
Template for pull requests                   | [Pull Request template] | [article](https://www.awesomecodereviews.com/pull-request-template/)
Template for notebooks                       | [Notebook template] |

## Set up the environment

1. Initialize git in local:

    ```bash
    make init_git
    ```

1. Set up the environment:

    ```bash
    make init_env
    ```

1. Install libraries for data science and machine learning:

    ```bash
    make install_data_libs
    ```

## Install dependencies

Agfter init the environment to install a new package, run:

```bash
poetry add <package-name>
```

Example to install [plotly](https://plotly.com/python/) in dev group:

```bash
poetry add plotly -G dev
```

## 🗃️ Project structure

```bash
.
├── codecov.yml                         # configuration for codecov
├── .code_quality
│   ├── bandit.yaml                     # bandit configuration
│   ├── mypy.ini                        # mypy configuration
│   └── ruff.toml                       # ruff configuration
├── data
│   ├── 01_raw                          # raw immutable data
│   ├── 02_intermediate                 # typed data
│   ├── 03_primary                      # domain model data
│   ├── 04_feature                      # model features
│   ├── 05_model_input                  # often called 'master tables'
│   ├── 06_models                       # serialized models
│   ├── 07_model_output                 # data generated by model runs
│   ├── 08_reporting                    # reports, results, etc
│   └── README.md                       # description of the data structure
├── docs                                # documentation for your project
├── .editorconfig                       # editor configuration
├── .github                             # github configuration
│   ├── actions
│   │   └── python-poetry-env
│   │       └── action.yml              # github action to setup python environment
│   ├── dependabot.md                   # github action to update dependencies
│   ├── pull_request_template.md        # template for pull requests
│   └── workflows
│       ├── docs.yml                    # github action to build documentation (mkdocs)
│       ├── pre-commit_autoupdate.yml   # github action update pre-commit hooks
│       └── test.yml                    # github action to run tests
├── .gitignore                          # files to ignore in git
├── Makefile                            # useful commands to setup environment,
├── models                              # store final models
├── notebooks
│   ├── 1-data                          # notebooks for data extraction and cleaning
│   ├── 2-exploration                   # notebooks for data exploration
│   ├── 3-analysis                      # notebooks for data analysis
│   ├── 4-feat_eng                      # notebooks for feature engineering
│   ├── 5-models                        # notebooks for model training
│   ├── 6-evaluation                    # notebooks for model evaluation
│   ├── 7-deploy                        # notebooks for model deployment
│   ├── notebook_template.ipynb         # template for notebooks
│   └── README.md                       # information about the notebooks
├── .pre-commit-config.yaml             # configuration for pre-commit hooks
├── pyproject.toml                      # dependencies for poetry
├── README.md                           # description of your project
├── src                                 # source code for use in this project
├── tests                               # test code for your project
└── .vscode                             # vscode configuration
    ├── extensions.json                 # list of recommended extensions
    └── settings.json                   # vscode settings
```

## Credits

This project was generated from [@JoseRZapata]'s [data science project template] template.

---
[@JoseRZapata]: https://github.com/JoseRZapata

[bandit]: https://github.com/PyCQA/bandit
[codecov]: https://codecov.io/
[Cookiecutter]:https://cookiecutter.readthedocs.io/stable/
[coverage.py]: https://coverage.readthedocs.io/
[Cruft]: https://cruft.github.io/cruft/
[data science project template]: https://github.com/JoseRZapata/data-science-project-template
[Data structure]: cover-letter-generation/data/README.md
[deepcheck]:https://deepcheck.io/
[dependabot]: https://github.com/dependabot/dependabot-core
[depy]:https://fpgmaas.github.io/deptry/
[DVC]:https://dvc.org/
[github actions]: https://github.com/features/actions
[hydra]: https://hydra.cc/
[Jupyter]:https://jupyter.org/
[Makefile]: https://www.gnu.org/software/make/manual/make.html
[MlFlow]:https://www.mlflow.org/
[Mypy]: http://mypy-lang.org/
[Notebook template]: cover-letter-generation/notebooks/notebook_template.ipynb
[NumPy]:https://numpy.org/
[OmegaConf]: https://omegaconf.readthedocs.io/en/latest/
[Pandas]:https://pandas.pydata.org/
[pandera]:(https://pandera.readthedocs.io/en/stable/)
[Poetry]: https://python-poetry.org/
[pre-commit]: https://pre-commit.com/
[Pull Request template]: cover-letter-generation/.github/pull_request_template.md
[Pyenv]: https://github.com/pyenv/pyenv
[pypi]: https://pypi.org/
[Pytest]: https://docs.pytest.org/en/latest/
[pyupgrade]: https://github.com/asottile/pyupgrade
[Ruff]: https://docs.astral.sh/ruff/
[scikit-learn]:https://scikit-learn.org/
