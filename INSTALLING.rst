Installing a Python environment
===============================

This short guide should get you set up with a local Python installation that
has all the packages you need for the SOLARNET summer school. If you encounter
any problems with these instructions, please get in touch with David Stansby
at d.stansby@ucl.ac.uk

Unfortunately the complete conda installation is not small, and it will take
up just under 2GB of space. However, installing it locally will give you a
python environment that you can continue to use after the summer school.

Step 1: Install miniconda
-------------------------
Conda is a package and environment management system for python. We'll use it
here to set up a new environment that contains all the packages you need.

To start, go to https://conda.io/projects/conda/en/latest/user-guide/install/index.html
and follow the installation instructions for your operating system. **Make sure
you choose Miniconda** - this will give you a minimal install, which we will add
to in the next step.

Step 2: Install packages
------------------------
1. Create a new directory which will contain the SOLARNET school resources.
2. Download https://raw.githubusercontent.com/dstansby/solarnet_connection_tutorial/main/environment.yml
   to this folder. If it shows up as a text file in your browser, just save
   the page to a file.
3. Open the terminal (Mac/Unix) or the anaconda prompt (Windows), and change to
   the directory created in step 1.


Next, run

.. code-block:: bash

  conda env create -f environment.yml --name solarnet

This will instruct conda to create a new environment, with the packages
specified in *environment.yml*. **This step can take a long time**,
so be patient.

To active the newly created environment, run:

.. code-block:: bash

  conda activate solarnet

This will activate the environment, giving you access to the installed packages.
To check that the environment is working, run:

.. code-block:: bash

  jupyter notebook

This should open a blank jupyter notebook in your browser.
