KiCad Mac Builder
=================

This is the 2017+ KiCad Mac builder and packager.  It does not yet work.  Do not use it to build or package.

It's close, though.

Setup
=====
When I run on MacOS, I need to do the following:

`brew install cmake swig glew glm cairo boost doxygen gettext wget`

Building by hand
================
To get up and running the absolute fastest, just use `build.sh`.  However, it builds everything and uses "reasonable" settings.  If you want something special, for now at least, run `cmake` and `make` by hand.  Better documentation is definitely welcomed, but for now, you can look at `build.sh` for reference.

Building inside a VM
====================
There can be value in building inside a VM.  This can help increase isolation and repeatability, by reducing the chances that something "sticks around" between builds, and helps reduce the chances of undocumented steps.  However, it can be slower and take more resources.

I do this, however, to make sure that people can build using 10.11, 10.12, and 10.13.  To do this, setup a macOS Vagrant machine.  I use https://github.com/timsutton/osx-vm-templates.  Please note, that as of early 2018, to create a 10.13 VM you must start with a 10.12 VM and upgrade it.

There is an example Vagrantfile and scripts in `vagrant/`.

Issues
======
In early 2018, I'm noticing that sometimes wxPython doesn't download properly from Sourceforge, so I've included a mirror in this repository.
