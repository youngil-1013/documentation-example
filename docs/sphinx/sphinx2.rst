Sphinx and RST 2: Deploying my Website on GitHub Pages
======================================================

Github Pages and Actions
------------------------

Right now, the "website" is just a bunch of HTML files in a directory, not accessible from the internet. To make it accessible, I will use GitHub Pages, which is linked with a GitHub repository and the service is free!
This section requires a GitHub account, which you can create at `GitHub <https:github.com>`_. If you have never authorized your computer to access GitHub, you will need to set up access tokens.
Create your access token by following the instructions at `GitHub's documentation <https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token>`_.

Now, create a new repository via GitHub, and make it public (required for GitHub Pages). You can name this repository anything you want, but because this doubles as my personal website, I name it "youngil-1013.github.io".
This allows me to directly access my website at `https://youngil-1013.github.io/ <https://youngil-1013.github.io/>`_. If not, you will need to access it via `https://<your-id>.github.io/<repository-name>`.

This section assumes that 1\) you have a GitHub account, 2\) you have created a repository, and 3\) you have set up an access token and can access GitHub from your computer. Furthermore, it assumes that you have named your repository `<your-id>.github.io`.`

Cloning the Repository and Cofiguration
----------------------------------------
The first step is to clone the repository to your local machine. I highly recommend to start the python virtual environment as we have done in the :ref:`setupfor-ubuntu`. You can do this by running the following command in your terminal:

.. code-block:: bash

  git clone <your-id>.github.io

You will initially see that the repository is empty (or at best, has a README file). Now, you will need to create a Sphinx project in the repository. We have already done something similar in the previous section:

.. code-block:: bash

  mkdir docs
  cd docs
  sphinx-quickstart

docs is the directory where Sphinx will look for the RST files. You can name this directory anything you want, but for me, I have named it "docs". Let us push what we have to Github. I would recommend creating a .gitignore file to ignore a few files that we do not want to push to GitHub:

.. code-block:: bash

  echo "_build/" > .gitignore # Ignores the build directory
  echo "docs/myenv/" >> .gitignore # If you are using a virtual environment
  echo ".vscode/" >> .gitignore # if you are using Visual Studio Code

.ignore files are used to ignore files that you do not want to push to Github. Depending on which IDE you are using, you may want to add more files to the .gitignore file. Now, let us push the changes to GitHub:

.. code-block:: bash

  git add .
  git commit -m "Initial commit"
  git push

Your repository should now be uploaded to `github.com/<your-id>.<your-id>.github.io`. Mine is at `https://github.com/youngil-1013/youngil-1013.github.io <https://github.com/youngil-1013/youngil-1013.github.io>`_
However, that's only the source code. We want to deploy the website. To do this, we will use Github Actions and Pages. First of all, 