Sphinx and RST 1: Introduction and Setup
========================================

Motivation
----------
Ever since I began programming, I have always wanted to have my own website where I could upload my projects, in a enjoyable but also informative way.

During the first year of my computer science journey at Yale-NUS College, 
I met Professor Olivier Danvy, who would always write his lecture notes in Sphinx, a documentation generator that coverts RST files into HTML. 
Following his footsteps, I decided to build my own website in Sphinx and RST and deploy the website using GitHub Pages.
Because this blog is about how I built the website and the nested blog in it, this blog a self-referential blog.
    
  `"This is not a self-referential sentence." <https://en.wikipedia.org/wiki/Liar_paradox>`_

RST and Sphinx
--------------
So what is this RST (or ReST) and Sphinx? RST is a markup language (think HTML and Markdown) that is used to write documents and define their formats.

Sphinx is a tool that takes markup files (RST and/or Markdown) and converts them into HTML, PDF, and other formats. 
Sphinx was originally built for RST, but as Markdown became more popular, they added support for it too.

In this blog, I will go through how I have set up Sphinx and RST to build this website.

Prerequisites
-------------
The full prerequisites can be found in the `Sphinx documentation <https://www.sphinx-doc.org/en/master/usage/installation.html>`_.
However, the main requirements are (code snippets are for Ubuntu):

* Python 3.X

  .. code-block:: bash
    
    sudo apt-get install python3

* python-is-python3 (optional, QoL)

  .. code-block:: bash

    sudo apt-get install python-is-python3
* Sphinx

  .. code-block:: bash

    sudo apt-get install python3-sphinx
* Python myst-parser package

  .. code-block:: bash

    sudo apt-get install python3-myst-parser
* A `Github <https://github.com/>`_ account