.. image:: https://media.quantopian.com/logos/open_source/alphalens-logo-03.png
    :align: center

Alphalens
=========
.. image:: https://github.com/quantopian/alphalens/workflows/CI/badge.svg
    :alt: GitHub Actions status
    :target: https://github.com/quantopian/alphalens/actions?query=workflow%3ACI+branch%3Amaster

Alphalens is a Python Library for performance analysis of predictive
(alpha) stock factors. Alphalens works great with the
`Zipline <https://www.zipline.io/>`__ open source backtesting library, and
`Pyfolio <https://github.com/quantopian/pyfolio>`__ which provides
performance and risk analysis of financial portfolios. You can try Alphalens
at  `Quantopian <https://www.quantopian.com>`_ -- a free,
community-centered, hosted platform for researching and testing alpha ideas. 
Quantopian also offers a `fully managed service for professionals <https://factset.quantopian.com>`_ 
that includes Zipline, Alphalens, Pyfolio, FactSet data, and more.

The main function of Alphalens is to surface the most relevant statistics
and plots about an alpha factor, including:

-  Returns Analysis
-  Information Coefficient Analysis
-  Turnover Analysis
-  Grouped Analysis

Note:
Fix bug to support python 3.10

Getting started
---------------

With a signal and pricing data creating a factor "tear sheet" is a two step process:

.. code:: python

    import alphalens
    
    # Ingest and format data
    factor_data = alphalens.utils.get_clean_factor_and_forward_returns(my_factor, 
                                                                       pricing, 
                                                                       quantiles=5,
                                                                       groupby=ticker_sector,
                                                                       groupby_labels=sector_names)

    # Run analysis
    alphalens.tears.create_full_tear_sheet(factor_data)


Learn more
----------

Check out the `example notebooks <https://github.com/quantopian/alphalens/tree/master/alphalens/examples>`__ for more on how to read and use
the factor tear sheet.  A good starting point could be `this <https://github.com/quantopian/alphalens/tree/master/alphalens/examples/alphalens_tutorial_on_quantopian.ipynb>`__

Installation
------------

Install with pip:

::

    pip install alphalens

Install with conda: 

::

    conda install -c conda-forge alphalens

Install from the master branch of Alphalens repository (development code):

::

    pip install git+https://github.com/quantopian/alphalens

Alphalens depends on:

-  `matplotlib <https://github.com/matplotlib/matplotlib>`__
-  `numpy <https://github.com/numpy/numpy>`__
-  `pandas <https://github.com/pandas-dev/pandas>`__
-  `scipy <https://github.com/scipy/scipy>`__
-  `seaborn <https://github.com/mwaskom/seaborn>`__
-  `statsmodels <https://github.com/statsmodels/statsmodels>`__

Usage
-----

A good way to get started is to run the examples in a `Jupyter
notebook <https://jupyter.org/>`__.

To get set up with an example, you can:

Run a Jupyter notebook server via:

.. code:: bash

    jupyter notebook

From the notebook list page(usually found at
``http://localhost:8888/``), navigate over to the examples directory,
and open any file with a .ipynb extension.

Execute the code in a notebook cell by clicking on it and hitting
Shift+Enter.

Questions?
----------

If you find a bug, feel free to open an issue on our `github
tracker <https://github.com/quantopian/alphalens/issues>`__.

Contribute
----------

If you want to contribute, a great place to start would be the
`help-wanted
issues <https://github.com/quantopian/alphalens/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22>`__.

Credits
-------

-  `Andrew Campbell <https://github.com/a-campbell>`__
-  `James Christopher <https://github.com/jameschristopher>`__
-  `Thomas Wiecki <https://github.com/twiecki>`__
-  `Jonathan Larkin <https://github.com/marketneutral>`__
-  Jessica Stauth (jstauth@quantopian.com)
-  `Taso Petridis <https://github.com/tasopetridis>`_

For a full list of contributors see the `contributors page. <https://github.com/quantopian/alphalens/graphs/contributors>`_

Example Tear Sheet
------------------

Example factor courtesy of `ExtractAlpha <https://extractalpha.com/>`_

.. image:: https://github.com/quantopian/alphalens/raw/master/alphalens/examples/table_tear.png
.. image:: https://github.com/quantopian/alphalens/raw/master/alphalens/examples/returns_tear.png
.. image:: https://github.com/quantopian/alphalens/raw/master/alphalens/examples/ic_tear.png
.. image:: https://github.com/quantopian/alphalens/raw/master/alphalens/examples/sector_tear.png
    :alt:
