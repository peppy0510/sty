
.. image:: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_logo.png
   :target: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_logo.png
   :align: center
   :alt: sty_logo

------------

.. image:: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_demo.png
   :target: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_demo.png
   :align: center
   :alt: sty_demo
   :width: 600px


Description
-----------

Simple, flexible and extensible string styling for your terminal.
Supports 3/4bit, 8bit and 24bit (truecolor, rgb) colors. Should work on
most Unix platfroms with most terminals. Recent versions of Windows 10
should work with this as well.

Sty comes with default color palettes and renderers, but you can easily
replace/customize them, without touching the markup.

Sty's goal is to provide Python with a little string styling markup, which
is decoupled from color palettes and terminal implementations.

Sty has no dependencies.

If you run into compatibility problems with sty, please file an issue!


Code Example
------------

.. code:: python

    from sty import fg, bg, ef, rs

    foo = fg.red + 'This is red text!' + fg.rs
    bar = bg.blue + 'This has a blue background!' + bg.rs
    baz = ef.italic + 'This is italic text' + rs.italic
    qux = fg(201) + 'This is pink text using 8bit colors' + fg.rs
    qui = fg(255, 10, 10) + 'This is red text using 24bit colors.' + fg.rs

    # Add custom colors:

    from sty import Style, RgbFg

    fg.orange = Style(RgbFg(255, 150, 50))

    buf = fg.orange + 'Yay, Im orange.' + fg.rs

    print(foo, bar, baz, qux, qui, buf, sep='\n')

The code above will print like this in the terminal:

.. image:: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_example.png
   :target: https://raw.githubusercontent.com/feluxe/sty/master/assets/README_example.png
   :align: center
   :alt: example
   :width: 600px


Documentation
-------------

Documentation-Website: https://sty.mewo.dev

Documentation-Website-Source: https://github.com/feluxe/sty-docs

