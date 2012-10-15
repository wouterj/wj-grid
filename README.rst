WjGrid
======

Welcome at WjGrid. This is a responsive grid written in SASS. It can be 
used as a static grid as well. It includes 5 grids that are somewhat based 
of the 978 grid system:

- 295
- 748
- 978
- 1105
- 1320

All of them have 12 columns, which makes it really easy to use responsive.

Grids
-----

Some details about the grids:

+--------+---------------+------------------+------------+
| system | device        | width of columns | guttersize |
+========+===============+==================+============+
| 295    | smartphones   | 20px             | 5px        |
+--------+---------------+------------------+------------+
| 748    | small tablets | 44px             | 20px       |
+--------+---------------+------------------+------------+
| 978    | old screens   | 54px             | 30px       |
+--------+---------------+------------------+------------+
| 1105   | new screens   | 60px             | 35px       |
+--------+---------------+------------------+------------+
| 1320   | TVs           | 73px             | 40xp       | 
+--------+---------------+------------------+------------+

Usage
-----

Load the CSS file
~~~~~~~~~~~~~~~~~

WjGrid prefers to work with a CSS precompressor. SASS is now supported, 
Stylus and LESS are comming soon.

WjGrid works with the ``wj-grid`` mixin:

.. code-block:: scss

    @import 'wj-grid/wj-grid';

    @include wj-grid;

This will load the default responsive grid system. If you want a static
grid system, you can add a parameter with the grid systems name:

.. code-block:: scss

    @import 'wj-grid/wj-grid';

    // includes the 1105 grid system
    @include wj-grid(1105);

HTML
~~~~

WjGrid will generate the classes ``.h1``, ``.h2``, ..., ``.h12`` and a ``.end``
and ``.parent`` class. You need to use it like this:

.. code-block:: html

    <!-- ... -->
    <div class="parent">
        <div class="h1">1</div>
        <div class="h2">2</div>
        <div class="h3">3</div>
        <div class="h6 end">6</div>

        <div class="h5">5</div>
        <div class="h7 end">7</div>
    </div>

The grids needs to be wrapped in a ``.parent`` element, which is the ``body`` 
element most of the time. The last element in a row should get a ``.end`` class.

Comming Soon
~~~~~~~~~~~~

- Stylus and LESS support;
- Vertical Grids.

Contributing
~~~~~~~~~~~~

I love contributors. We can get amazing ideas and the best, allround comptable, 
code as possible!

Coding
~~~~~~

Fork this repo, create a new branch and start working on the code. Push
it to github if you are finished and create a Pull Request.

Ideas
~~~~~

Ideas are welcome too, just make an issue and start the issue name with ``[Feature]``.
