
backtrader
==========

.. image:: https://img.shields.io/pypi/v/backtrader.svg
   :alt: PyPi Version
   :scale: 100%
   :target: https://pypi.python.org/pypi/backtrader/

..  .. image:: https://img.shields.io/pypi/dm/backtrader.svg
       :alt: PyPi Monthly Donwloads
       :scale: 100%
       :target: https://pypi.python.org/pypi/backtrader/

.. image:: https://img.shields.io/pypi/l/backtrader.svg
   :alt: License
   :scale: 100%
   :target: https://github.com/mementum/backtrader/blob/master/LICENSE
.. image:: https://travis-ci.org/mementum/backtrader.png?branch=master
   :alt: Travis-ci Build Status
   :scale: 100%
   :target: https://travis-ci.org/mementum/backtrader
.. image:: https://readthedocs.org/projects/backtrader/badge/?version=latest
   :alt: Documentation Status
   :scale: 100%
   :target: https://readthedocs.org/projects/backtrader/
.. image:: https://img.shields.io/pypi/pyversions/backtrader.svg
   :alt: Pytghon versions
   :scale: 100%
   :target: https://pypi.python.org/pypi/backtrader/


**Release 1.7.0.93**: `TA-Lib integration
<http://www.backtrader.com/posts/2016-07-26-talib-integration/talib-integration/>`_

Features:
=========

Live Trading and backtesting platform written in Python.

  - Live Data Feed and Trading with Interactive Brokers (needs ``IbPy`` and
    benefits greatly from an installed ``pytz``)
  - Data feeds from csv/files or for example *pandas*
  - Filters for datas (like breaking a daily bar into chunks to simulate intraday)
  - Multiple data feeds and multiple strategies supported
  - Multiple timeframes at once
  - Integrated Resampling and Replaying
  - Step by Step backtesting or at once (except in the evaluation of the Strategy)
  - Integrated battery of indicators
  - TA-Lib indicator support
  - Easy development of custom indicators
  - Analyzers (for example: TimeReturn, Sharpe Ratio, SQN) and ``pyfolio``
    integration
  - Flexible definition of commission schemes
  - Integrated broker simulation with Market, Close, Limit, Stop and StopLimit
    orders and continuous cash adjustmet for future-like instruments
  - Plotting (requires matplotlib)

Documentation
=============

The blog:

  - `backtrader blog <http://www.backtrader.com>`_

Read the full documentation at readthedocs.org:

  - `backtrader documentation <http://backtrader.readthedocs.io/>`_

List of built-in Indicators (93)

  - `backtrader indicators <http://backtrader.readthedocs.io/indautoref.html>`_

Python 2/3 Support
==================

  - Python 2.7
  - Python 3.2/3.3/3.4/3.5

  - It also works with pypy and pypy3 (no plotting - matplotlib is not supported under pypy)

Compatibility is tested during development with 2.7 and 3.4

The other versions are tested automatically with Travis.

Installation
============

``backtrader`` is self-contained with no external dependencies (except if you
want to plot)

From pypi:

  - pip install backtrader

  - pip install backtrader[matplotlib]

    If `matplotlib` is not installed and you wish to do some plotting

.. note:: The minimum matplotlib version is 1.4.1

For IB Trading:

  - ``IbPy`` doesn't seem to be in PyPi. Do either::

      pip install git+https://github.com/blampe/IbPy.git

    or (if ``git`` is not available in your system)::

      pip install https://github.com/blampe/IbPy/archive/master.zip

From source:

  - Place the *backtrader* directory found in the sources inside your project

Version numbering
=================

X.Y.Z.I

  - X: Major version number. Should stay stable unless something big is changed like an
    overhaul to use numpy
  - Y: Minor version number. To be changed upon adding a complete new feature or
    (god forbids) an incompatible API change.
  - Z: Revision version number. To be changed for documentation updates, small
    changes, small bug fixes
  - I: Number of Indicators already built into the platform

Alternatives
============

If after seeing the docs (see also the example below) you feel this is not your
cup of tea, you can always have a look at similar Python platforms:

  - `PyAlgoTrade <https://github.com/gbeced/pyalgotrade>`_
  - `Zipline <https://github.com/quantopian/zipline>`_
  - `Ultra-Finance <https://code.google.com/p/ultra-finance/>`_
  - `ProfitPy <https://code.google.com/p/profitpy/>`_
  - `pybacktest <https://github.com/ematvey/pybacktest>`_
  - `prophet <https://github.com/Emsu/prophet>`_
  - `quant <https://github.com/maihde/quant>`_
  - `AlephNull <https://github.com/CarterBain/AlephNull>`_
  - `Trading with Python <http://www.tradingwithpython.com/>`_
  - `visualize-wealth <https://github.com/benjaminmgross/visualize-wealth>`_
  - `tia: Toolkit for integration and analysis
    <https://github.com/bpsmith/tia>`_
  - `QuantSoftware Toolkit
    <http://wiki.quantsoftware.org/index.php?title=QuantSoftware_ToolKit>`_
  - `Pinkfish <http://fja05680.github.io/pinkfish/>`_
  - `bt <http://pmorissette.github.io/bt/index.html>`_

     ``bt`` slightly pre-dates ``backtrader`` and has a completely different
     approach but it is funny *bt* was also chose as the abbreviation for
     ``backtrader`` during imports and that some of the methods have the same
     naming (obvious naming anyhow): "run, plot ..."
