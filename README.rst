|CI Build Status| |PyPI Version| |Python Versions|


UFO Extractor
=============

Tools for extracting data from font binaries into UFO objects.

Features
--------

Import data into a `Defcon <https://github.com/typesupply/defcon>`__ ``Font``
instance:

.. code:: python

   >>> import extractor
   >>> import defcon
   >>> ufo = defcon.Font()
   >>> extractor.extractUFO("/path/to/MyFont.ttf", ufo)
   >>> ufo.save("/path/to/MyFont.ufo")

Supported input formats:

-  CFF or TrueType-flavored OpenType fonts (``*.otf``, ``*.ttf``)
-  `FontTools <https://github.com/fonttools/fonttools>`__ TTX files
   (``*.ttx``)
-  WOFF 1.0/2.0 (``*.woff``, ``*.woff2``)
-  PostScript Type1 fonts (``*.pfa``, ``*.pfb``, etc.)
-  FontLab files (``*.vfb``, when installed with optional dependency "vfb")

Installation
------------

You can install ``extractor`` with ``pip``:

.. code::

   $ pip install ufo-extractor

To install with support for extracting from vfb files:

.. code::

   $ pip install ufo-extractor[vfb]

Note that, for historical reasons, the package is listed on the
`Python Package Index <https://travis-ci.org/typesupply/extractor>`__ under the name
``ufo-extractor``, to disambiguate it from another package also called "extractor".
However, the import name for the package remains ``extractor``, without prefix.


.. |CI Build Status| image:: https://github.com/robotools/extractor/workflows/Tests/badge.svg
   :target: https://github.com/robotools/extractor/actions?query=workflow%3ATests
.. |PyPI Version| image:: https://img.shields.io/pypi/v/ufo-extractor.svg
   :target: https://pypi.org/project/ufo-extractor/
.. |Python Versions| image:: https://img.shields.io/badge/python-3.7%2C%203.8%2C%203.9%2C%203.10-blue.svg
