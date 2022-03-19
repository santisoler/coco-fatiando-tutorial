# CoCo2022: Learning how to use Fatiando tools
_by [Santiago Soler](https://github.com/santisoler/), [Agustina Pesce](https://github.com/aguspesce/) and [Andrea Balza](https://github.com/andieie)_


## About

In this tutorial we’ll take a tour around
[Fatiando a Terra](https://www.fatiando.org) tools.
The project is composed by different open-source Python libraries, each one with a specific goal and set of problems that they tackle.

In this notebook we will learn how we can use the Fatiando a Terra tools to process gravity data (or any spatial data).
We will start with a real dataset of scattered gravity observations
and finally produce a regular grid of the Bouguer gravity disturbance.

## Setup

There two way to follow this tutorial:

- Use [JupyterHub](https://lab.openearthscape.org) where the notebook in this repository can be run
- Or run the notebook in your computer.

### Run it in your computer

There are a few things you'll need to run the notebook:

1. A working Python installation ([Anaconda](https://www.anaconda.com/) or Miniconda)
2. The fatiando tutorial _conda environment_ installed
3. A web browser that works with Jupyter notebooks
   (basically anything except Internet Explorer)

#### Step 1 - Install a Python distribution

In this tutorial we will be using the [Anaconda](https://www.anaconda.com/)
Python distribution along with the `conda` package manager. If you already have
Anaconda or Miniconda installed, you can skip this step.

If not, please follow the instructions for getting Anaconda up and running in
your system: https://docs.anaconda.com/anaconda/install/

If you need more help to install Anaconda you can see
[this video tutorial of Software Carpentry](https://carpentries.github.io/workshop-template/#python).

#### Step 2 - Create the `coco-fatiando` conda environment

Now you could install all the dependencies through the `conda` package manager:

```
conda env create -f environment.yml
```

And then activate the environment:

```
conda activate coco-fatiando
```

#### Step 3 - Start JupyterLab

**Windows users:** Make sure you set a default browser that is **not Internet Explorer**.

Activate the conda environment:

```
conda activate coco-fatiando
```

Start the JupyterLab server:

```
jupyter lab
```

Jupyter should open in your default web browser.
We'll start from here in the tutorial and create a new notebook together.

If you need more help to run JupyterLab you can see [this lesson of Software Carpentry](https://swcarpentry.github.io/python-novice-gapminder/01-run-quit/index.html).

## License

The notebook in this repo is a modified version of the one present in
[fatiando/tutorials](https://github.com/fatiando/tutorials) available under the
BSD 3-clause license.

All Python source code is made available under the BSD 3-clause license. You
can freely use and modify the code, without warranty, so long as you provide
attribution to the authors.

Unless otherwise specified, all figures and Jupyter notebooks are available
under the Creative Commons Attribution 4.0 License (CC-BY).

The full text of these licenses is provided in the LICENSE.txt file.
