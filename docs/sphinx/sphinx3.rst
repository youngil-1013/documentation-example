Sphinx and RST 3: Hello World
=============================

There are two ways to approach Sphinx and RST. The first is to learn how Sphinx generates documentation from RST files first (top-down). The second is to learn how to write RST files first (bottom-up). Because I am `against top-down <https://www.change.org/p/nus-president-prof-tan-eng-chye-nus-reverse-the-mergers-and-nomoretopdown>`_ methods, let's first dicuss what RST is and how to write RST files.
As discussed during in :ref:`motivation`, RST is a markup language, similar to HTML and Markdown. While less popular than Markdown, RST is more powerful and offers more customization. For example, you can create tables, footnotes, and even math equations in RST, natively.
To create a new RST file, create a new file with the extension .rst. For example, if you want to create a new file called "hello.rst", you can do so by running the following command in your terminal:

.. code-block:: bash

  touch hello.rst

Open it up and you will see that there is nothing in the file. To create a title, subtitle, 

.. code-block:: rst

  Hello World
  ===========

  This is a subtitle
  ------------------

  This is a subsubtitle
  ~~~~~~~~~~~~~~~~~~~~~

