# py-template

Template repository for Python projects.

This repository contains all of the basic tools and files common to most Python projects I use day to day. It contains tools needed to build a new conda environment in the project using `anaconda-project`, for pairing Jupyter notebooks to `jupytext` myst-md files, etc.

## Major packages:
* Jupytext : Pair notebooks with myst-md files for smaller repo commits, without the nasty version control changelog from ipynb metadata changing. The myst-nb format also allows autobuilding of notebooks into documentation with Sphinx.
* Anaconda-Project : Project and environment management package.
* Sphinx : Documentation and static website builder.

```
|py-template/ Root Directory
|
|---Docs/             : Directory for notebooks and site deployment
|    |---Notebooks    : Location for jupyter notebooks, paired to myst markdown
|    |---build        : Sphinx site autogenerate location
|    |---conf.py      : Sphinx site config file and extensions manager
|    |---index.md     : Sphinx config index for specifying files to include
|    |---Notebooks.md : Example Sphinx config file for including subdirectory Notebook
|
|---src/              : Directory to keep all python modules. Try to keep root clean
|    |---module1/     : Example module dir
|    |---module2/     : Example module dir
|
|---tests/            : Directory for pytest modules. Run using make tests
|
|---_ext/             : Directory to clone dependencies that must be built from source
|
|---Makefile          : Contains various build commands for ease of use.
|---.gitignore        : Files to ignore per repo. Included by .hgignore, just in case.
|---pyproject.toml    : Python project standard configuration file.
|---.coveragerc       : pytest-cov configuration file.
|---.nojekyll         : Bypasses certain build steps when deployed on GitHub pages.
|---anaconda-project.yaml
```
