# Avazu CTR Outlier Detection Challenge

## What is this?

This repository contains a solution for the Avazu CTR Outlier Detection challenge. The avazu_outlier_detection.ipynb file contains the solution and below you can read instructions on how to open the notebook.

## How can I run this?

You will have to make a copy of this repository on your machine first. Use the git cli to clone it:

> git clone https://github.com/kersanszki-levente/avazu-ctr-outlier-detection.git

The notebook assumes a Python 3.6 installation with a couple of dependencies. On CentOS 7 Python can be installed using yum along with the Python development tools (necessary for certain dependencies) and pip (the de facto package manager for Python):

> yum install python36 python36-devel python36-pip

Specific dependencies are listed in the requirements.txt file and can be passed to pip for installation:

> pip install -r requirements.txt

To view and start the notebook on a local machine just start a jupyter notebook service from the project directory:

> jupyter notebook

## Acquiring the data

The notebook assumes the existence of the avazu ctr challenge dataset on your machine, which can be downloaded using the kaggle cli. The cli is tool is automatically installed with the dependencies above. However you will have to setup your kaggle account first and making sure that you have your credentials setup properly on your system. You can follow the instructions at the [Kaggle API Github page](https://github.com/Kaggle/kaggle-api). You can acquire the datasets using the tool:

> kaggle competitions download -c avazu-ctr-prediction

The downloaded file will be a zip file which you can decompress with unzip and then discard it:

> unzip avazu-ctr-prediction.zip  
> rm avazu-ctr-prediction.zip

The unzipped data files will be compressed with gunzip, but the notebook relies on pandas to take care of that during runtime. Make sure that you copy the downloaded files to the data directory or - if you have a dedicated place for large files elsewhere in your system - use a symbolic link instead:

> ln -s [source] [destination]