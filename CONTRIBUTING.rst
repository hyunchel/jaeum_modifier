Contribution Guide
==================

In case someone wish to contribute to this repository:

- Any bug fixes or additional features via PR is welcome.
- More tests are always welcome.
- Use issues to create a bug report or a feature request.

Coding Style
------------
In general, try to follow  `Pocoo Style Guide`_.
For function doc trings, the original Sphinx syntax:

.. code-block:: python

    def format_exception(etype, value, tb[, limit=None]):
        """Format the exception with a traceback.

        :param etype: exception type
        :param value: exception value
        :param tb: traceback object
        :param limit: maximum number of stack frames to show
        :type limit: integer or None
        :rtype: list of strings
        """

Only `:param` and `:return` are required if exist.

.. _Pocoo Style Guide: http://www.pocoo.org/internal/styleguide/
