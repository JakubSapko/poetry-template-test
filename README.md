# INT DA Project template

A Python project template tailored for INT DA team's needs.

## Features

- Poetry - dependency and project management
- Pytest and tox for testing and test orchestration (coverage and pytest-cov are optional)
- Black and isort - code formatting
- flake8 - code linting
- mypy - static type checking
- pre-commit - general code quality


Multiple Python versions are supported (^3.8).

## Requirements
To use this template you'll need
- Python ^3.8
- [Poetry ^1.3.2](https://python-poetry.org/)
- [pre-commit](https://pre-commit.com/)


## Using the template

To use this repo as a project template select this repository as a default template when creating new repository from the GitHub view or clone it into your project locally.

```bash
# Install all dependencies
poetry install --sync --all-extras --with dev,test,coverage

# install git hook scripts for development
pre-commit install

# Other useful installation dependencies commands

# Install dependencies with all extras
poetry install --all-extras
# Only install required dependencies for production
poetry install

# Specify python version
poetry env use python3.9
```

### Available commands

```bash

# Debug "hello" project with ipdb3
poetry run ipdb3 ./src/hello/main.py

# Code test
poetry run pytest -s

# Run default coverage test
poetry run tox

# Run "hello" sample project coverage test at python 3.9 and 3.10
poetry run tox -e py{39,310}-hello

# Lint with black
poetry run black ./src --check

# Format code with black
poetry run black ./src

# Check with mypy
poetry run mypy ./src

# Check import order with isort
poetry run isort ./src --check

# Lint with flake8
poetry run flake8 ./src
```

Feel free to add custom commands that will fit your project-specific needs, this template is just a canvas for adding more things to it.
