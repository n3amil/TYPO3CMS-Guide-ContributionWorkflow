.. include:: ../Includes.txt

.. highlight:: bash


.. _prerequisites:

==============================
Prerequisites and useful tools
==============================

Here's a list of the tools we use in the TYPO3 project.
If some of these are new for you, take a few minutes to read up about what they
do for us. Maybe they prove useful in your everyday work as well.
You can find installation tutorials in the :ref:`Appendix <appendix>` section.

Composer
========

.. sidebar:: Composer

   You can learn a lot more about composer on their website https://getcomposer.org/.

Composer is a dependency manager for PHP.

So what it basically does is find packages you have defined to be part of your application (in our case TYPO3). But what
if these packages rely on other packages as well? This is where composer jumps in and takes care of keeping all these
packages in sync.

Since we use quite some packages (because why would we invent things ourselves that are already there?) composer is an
extremely useful tool for us.

Composer is a mandatory tool for setting up your toolchain for TYPO3. Follow the
installation instructions from https://getcomposer.org. Afterwards, you should
have a working executable `composer` available.

Verify composer is working::

   $ composer --version


Setting up your frontend build toolchain.
=========================================

Yarn
---------------

TYPO3 itself does not need yarn to run, but yarn is something similar to composer, but for the world outside of PHP.
We will be mainly using yarn to get helpful tools like Grunt and Bower.

Install on MacOS
~~~~~~~~~~~~~~~~

1. install the packagemanager homebrew::

      /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

2. install yarn::

      brew install yarn


Installer for Windows and MacOS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Go to https://yarnpkg.com/lang/en/docs/install/#windows-tab

2. Download the package and install


Linux
~~~~~

1. Go to https://yarnpkg.com/lang/en/docs/install/#linux-tab

2. Download the package and install

For additional infos see https://yarnpkg.com


Install all required packages
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The later section :ref:`yarn-build` will explain how to set
everything up in your TYPO3 working directory.

Grunt
=====

.. sidebar:: Grunt

   You can learn more about Grunt on their website http://gruntjs.com/.

Grunt is a JavaScript-based task runner. While this does not sound very expressive at first this is basically, what grunt
does - it runs tasks for us.

In our case grunt compiles CSS from LESS, minifies and concatenates JavaScript files, runs syntax checks and a couple of
other useful things. The good news is that TYPO3 comes with a predefined set of tasks that grunt will run, so you don't
have to take care of all the busywork underneath.


