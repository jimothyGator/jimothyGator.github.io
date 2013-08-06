---
layout: page
title: "Getting Started with Python on Debian or Ubuntu Linux"
date: 2013-08-02 14:49
comments: true
sharing: true
footer: true
---
Debian and Ubuntu Linux come with Python installed, but the version may be out-of-date. These instructions describe 
how to install the latest version in the Python 2.x line, as well as some other goodies for Python
development.

Check Python Version
--------------------

Run the following command:

	python --version

If it reports "Python 2.7.x", you're already up-to-date and don't need to follow the rest of these instructions.


Update Apt Packages
-------------------

In a terminal shell, run the following:

	sudo apt-get update


Build Python from Source
------------------------

Run the following commands:

	sudo apt-get install -y build-essential libsqlite3-dev zlib1g-dev libncurses5-dev libgdbm-dev libbz2-dev libreadline5-dev libssl-dev libdb-dev
	wget http://www.python.org/ftp/python/2.7.5/Python-2.7.5.tgz
	tar -xzf Python-2.7.5.tgz
	cd Python-2.7.5
	./configure --prefix=/opt/python27 --enable-shared
	make
	sudo make install





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

	