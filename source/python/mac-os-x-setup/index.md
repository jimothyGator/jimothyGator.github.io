---
layout: page
title: "Getting Started with Python on Mac OS X"
date: 2013-08-02 09:02
comments: true
sharing: true
footer: true
---
Mac OS X comes with Python installed, but the version may be out-of-date. These instructions describe 
how to install the latest version in the Python 2.x line, as well as some other goodies for Python
development.

Installing Python via Homebrew has other advantages, as well. In particular, it means you don't need to run `sudo`
each time you install a new Python package, making your life as a developer easier.

Install Homebrew
----------------

[Homebrew](http://brew.sh) is "the missing package manager for Mac OS X." It's similar to Linux package
managers such as apt on Debian and Ubuntu, or Yum on RHEL and CentOS. 

We're going to install Homebrew so we can install other stuff. To do so, open a Terminal window and run
the following command (copy the line, paste it into Terminal, then hit return):

	ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"


Install Python
--------------

With Homebrew now installed, installing an up-to-date Python is easy. In the terminal, simply run:

	brew install python

Check that it is installed correctly by running:

	python --version

This should print `Python 2.7.5` (or later; 2.7.5 was the latest at the time this was written).

This also installs Pip, a Python package manager. You can verify that by running:

	pip --version

It should print something like `pip 1.4 from /usr/local/lib/python2.7/site-packages/pip-1.4-py2.7.egg (python 2.7)`.


Install Virtualenv
------------------
"[Virtualenv](http://www.virtualenv.org/en/latest/) is a tool to create isolated Python environments." In other words, while you're fiddling around with Python, you don't have to worry about screwing things up. :) There's more to it than that, but that explanation should suffice for now.

Run the following commands in Terminal:

	pip install virtualenv
	pip install virtualenvwrapper
	source /usr/local/bin/virtualenvwrapper.sh

Also, put the last line (`source /usr/local/bin/virtualenvwrapper.sh`) in your `.bashrc`, `.bash_profile`, `.zshrc`, etc. so virtualenvwrapper is automatically loaded when you open a new Terminal shell.


Install IPython
---------------

[IPython](http://ipython.org) is an interative shell, and is an improvement to the shell that comes with Python. 

In the Terminal, run:

	pip install ipython

Try it out:

	ipython

	In [1]: print "Hello, world!"
	Hello, world!

Great job! You'll now set up to learn and play with Python.

	