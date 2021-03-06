PyKEEN |build| |coverage| |docs| |zenodo|
=========================================

PyKEEN (Python KnowlEdge EmbeddiNgs) is a package for training and evaluating knowledge graph embeddings. Currently,
it provides implementations of 10 knowledge graph emebddings models, and can be run in *training mode* in which users
provide their own set of hyper-parameter values, or in *hyper-parameter optimization mode* to find suitable
hyper-parameter values from set of user defined values. PyKEEN can also be run without having experience in programing
by using its interactive command line interface that can be started with the command *pykeen* from a terminal.

Citation
--------
If you find PyKEEN useful in your work, please consider citing:

.. [1] Ali, M., *et al.* (2018). `BioKEEN: A library for learning and evaluating biological knowledge graph embeddings
       <https://doi.org/10.1101/475202>`_. bioRxiv 475202.

Installation |pypi_version| |python_versions| |pypi_license|
------------------------------------------------------------
``pykeen`` can be installed on any system running Python 3.6+ with the following command:

.. code-block:: sh

    pip install pykeen

Alternatively, it can be installed from the source for development with:

.. code-block:: sh

    $ git clone https://github.com/SmartDataAnalytics/PyKEEN.git pykeen
    $ cd pykeen
    $ pip install -e .

However, GPU acceleration is limited to Linux systems with the appropriate graphics cards
as described in the PyTorch documentation.

Usage
-----
Code examples can be found in the `notebooks directory
<https://github.com/SmartDataAnalytics/PyKEEN/tree/master/notebooks>`_.

CLI Usage - Set Up Your Experiment within 60 seconds
----------------------------------------------------
To start the PyKEEN CLI, run the following command:

.. code-block:: sh

    pykeen

then the command line interface will assist you to configure your experiments.

To start PyKEEN with an existing configuration file, run:

.. code-block:: sh

    pykeen -c /path/to/config.json

then the command line interface won't be called, instead the pipeline will be started immediately.

Starting the Prediction Pipeline
********************************
To make prediction based on a trained model, run:

.. code-block:: sh

    pykeen-predict -m /path/to/model/directory -d /path/to/data/directory

Summarize the Results of All Experiments
****************************************
To summarize the results of all experiments, run:

.. code-block:: sh

    pykeen-summarize -d /path/to/experiments/directory -o /path/to/output/file.csv

.. |build| image:: https://travis-ci.org/SmartDataAnalytics/PyKEEN.svg?branch=master
    :target: https://travis-ci.org/SmartDataAnalytics/PyKEEN
    :alt: Build Status

.. |zenodo| image:: https://zenodo.org/badge/136345023.svg
    :target: https://zenodo.org/badge/latestdoi/136345023
    :alt: Zenodo DOI

.. |docs| image:: http://readthedocs.org/projects/pykeen/badge/?version=latest
    :target: https://pykeen.readthedocs.io/en/latest/
    :alt: Documentation Status

.. |python_versions| image:: https://img.shields.io/pypi/pyversions/pykeen.svg
    :alt: Supported Python Versions: 3.6 and 3.7

.. |pypi_version| image:: https://img.shields.io/pypi/v/pykeen.svg
    :alt: Current version on PyPI

.. |pypi_license| image:: https://img.shields.io/pypi/l/pykeen.svg
    :alt: MIT License

.. |coverage| image:: https://codecov.io/gh/SmartDataAnalytics/PyKEEN/branch/master/graphs/badge.svg
    :target: https://codecov.io/gh/SmartDataAnalytics/PyKEEN
    :alt: Coverage Status on CodeCov
