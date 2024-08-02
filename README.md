# Packaging Tutorial

This is a simple packaging tutorial for Python projects.

```shell
packaging-tutorial $ tree .
.
├── LICENSE
├── README.md
├── pyproject.toml
└── src
    └── packaging_tutorial
        ├── hello.py
        └── __init__.py
```

## Getting started

```shell
pipenv install
```

## Generate distribution archives

```
pipenv run python -m build
```

You should have the `dist` directory generated with the following files:
```shell
packaging-tutorial $ tree .
.
├── dist
│   ├── pkg_packaging_tutorial-0.0.1-py3-none-any.whl
│   └── pkg_packaging_tutorial-0.0.1.tar.gz
(...)
```

## Uploading to our index

```shell
pipenv run twine upload dist/*
```

## Using it in a project

```shell
pipenv install pkg-packaging-tutorial
```
