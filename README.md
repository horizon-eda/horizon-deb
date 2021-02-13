# Horizon EDA packages for Ubuntu and Debian

To make Horizon EDA easier to install on Debian and Ubuntu, this repository uses Actions to build Debian packages and publish them on packagecloud.io.

See [the installation instructions](https://horizon-eda.readthedocs.io/en/latest/installation.html#debian-ubuntu) for how to install it.

The debian packaging files located in `debian` are derived from the [Debian-maintained package](https://packages.debian.org/sid/horizon-eda).
Compared to the Debian-maintained package, this package omits:

 - Doxygen-generated documentation
 - READMEs in `/usr/share/doc`
 - The python module
