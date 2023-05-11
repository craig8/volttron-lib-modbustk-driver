# volttron-lib-modbustk-driver

![Eclipse VOLTTRON™](https://img.shields.io/badge/Eclipse%20VOLTTRON™-10.0.4rc-red.svg)
![Python 3.10](https://img.shields.io/badge/python-3.10-blue.svg)
![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)
[!Passing?](https://github.com/VOLTTRON/volttron-lib-modbustk-driver/actions/workflows/run-tests.yml/badge.svg)
[![pypi version](https://img.shields.io/pypi/v/volttron-lib-modbustk-driver.svg)](https://pypi.org/project/volttron-lib-modbustk-driver/)

## Prerequisites

* Python 3.10+
* Eclipse VOLTTRON<sup>tm</sup> 10.0+

### Python

<details>
<summary>To install Python 3.10, we recommend using <a href="https://github.com/pyenv/pyenv"><code>pyenv</code></a>.</summary>

```bash
# install pyenv
git clone https://github.com/pyenv/pyenv ~/.pyenv

# setup pyenv (you should also put these three lines in .bashrc or similar)
export PATH="${HOME}/.pyenv/bin:${PATH}"
export PYENV_ROOT="${HOME}/.pyenv"
eval "$(pyenv init -)"

# install Python 3.8
pyenv install 3.10

# make it available globally
pyenv global system 3.10
```
</details>


### Poetry

This project uses `poetry` to install and manage dependencies. To install poetry,
follow these [instructions](https://python-poetry.org/docs/master/#installation).

# Installation

With `pip`:

```shell
python3.10 -m pip install volttron-lib-modbustk-driver

# Develop mode
python3.10 -m pip install --editable volttron-lib-modbustk-driver
```

## Development

### Environment

Set the environment to be in your project directory:

```poetry config virtualenvs.in-project true```

If you want to install all your dependencies, including dependencies to help with developing your agent, run this command:

```poetry install```

If you want to install only the dependencies needed to run your agent, run this command:

```poetry install --no-dev```

Activate the virtual environment:

```shell
# using Poetry
poetry shell

# using 'source' command
source "$(poetry env info --path)/bin/activate"
```

### Source Control

1. To use git to manage version control, create a new git repository in your local agent project.

```git init```

2. Then create a new repo in your Github or Gitlab account. Copy the URL that points to that new repo in
your Github or Gitlab account. This will be known as our 'remote'.

3. Add the remote (i.e. the new repo URL from your Github or Gitlab account) to your local repository. Run the following command:

```git remote add origin <my github/gitlab URL>```

When you push to your repo, note that the default branch is called 'main'.


### Optional Configurations

#### Precommit

Note: Ensure that you have created the virtual environment using Poetry

Install pre-commit hooks:

```poetry run pre-commit install```

To run pre-commit on all your files, run this command:

```poetry run pre-commit run --all-files```

If you have precommit installed and you want to ignore running the commit hooks
every time you run a commit, include the `--no-verify` flag in your commit. The following
is an example:

```git commit -m "Some message" --no-verify```


## Documentation

To build the docs, navigate to the 'docs' directory and build the documentation:

```shell
cd docs
make html
```

After the documentation is built, view the documentation in html form in your browser.
The html files will be located in `~<path to project directory>/docs/build/html`.

**PROTIP: To open the landing page of your documentation directly from the command line, run the following command:**

```shell
open <path to project directory>/docs/build/html/index.html
```

This will open the documentation landing page in your default browsert (e.g. Chrome, Firefox).
