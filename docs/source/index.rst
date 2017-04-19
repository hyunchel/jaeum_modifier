.. jaeum_modifier documentation master file, created by
   sphinx-quickstart on Sun Mar 19 15:32:49 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Jaeum Modifier
==============

`jaeum_modifier` module modifies a single Jaeum of a Hangul syllable among the given Hangul word or sentence.


Examples
--------

Modify a single syllable chosen by an index.

.. code-block:: python

    from jaeum_modifier import modify
    message = u'안녕하세요'
    print(modify(message, index=1, jaeum=u'ㅉ')) # 안쪙하세요

``jaeum_modifier.modify`` replaces Jaeum of the indexed syllable to the given Jaeum(``JJ(u'ㅉ')``).

Set multiple syallables by the complexity.

.. code-block:: python

    from jaeum_modifier import modify_by_complexity
    message = u'안녕하세요'
    print(modify_by_complexity(message, jaeum=u'ㅉ', complexity=2)) # 안녕짜쩨쬬

By ``complexity`` we mean the number of Jamos that is used to make up a syllable.
In the example above, we choose all syllables with complexity of 2.
Looking at the example message(``u'안녕하세요'``), we see complexities of ``3 3 2 2 2``.
Thus, only the last three syllables are modified.


Installation
------------

Jaeum Modifier can be installed via ``pip``:

.. code-block:: console

    $ pip install jaeum-modifier

You can also install from `Github repository`__:

.. code-block:: console

    $ git clone git@github.com:hyunchel/jaeum_modifier.git
    $ cd jaeum_modifier
    $ python setup.py install
      
.. _Jaeum Modifier: https://github.com/hyunchel/jaeum_modifier
__ https://github.com/hyunchel/jaeum_modifier


Community
---------

There is no community for this project.



License
-------
`jaeum_modifier` is under MIT License.
For more information, please see `LICENSE`_.

.. _LICENSE: https://github.com/hyunche/LICENSE



Reference
=========

* :ref:`genindex`
* :ref:`search`

Interface
---------
.. autofunction:: jaeum_modifier.modify
.. autofunction:: jaeum_modifier.modify_all
.. autofunction:: jaeum_modifier.modify_by_complexity

Exceptions
----------
.. autoexception:: jaeum_modifier.InvalidHangulError
.. autoexception:: jaeum_modifier.InvalidJaeumError
.. autoexception:: jaeum_modifier.NoComplexityFoundError
.. autoexception:: jaeum_modifier.NoIndexFoundError

Summary
-------
.. autosummary::
    jaeum_modifier.modify
    jaeum_modifier.modify_all
    jaeum_modifier.modify_by_complexity
    jaeum_modifier.InvalidHangulError
    jaeum_modifier.InvalidJaeumError
    jaeum_modifier.NoComplexityFoundError
    jaeum_modifier.NoIndexFoundError
