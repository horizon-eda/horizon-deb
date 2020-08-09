# Horizon EDA packages for Ubuntu and Debian

To make Horizon EDA easier to install on Debian and Ubuntu, this repository uses Actions to build Debian packages and publish them on Bintray.

These packages are currently considered to be experimental and might change without notice as I haven't been able to test them on an actual Debian / Ubuntu system.

To install the packages, you'll need to add one of these lines to your `/etc/apt/sources.list`

```
# Debian Buster
deb https://dl.bintray.com/carrotindustries/horizon-eda-buster horizon-eda-buster main

# Ubuntu Bionic
deb https://dl.bintray.com/carrotindustries/horizon-eda-bionic horizon-eda-bionic main

# Ubuntu Focal
deb https://dl.bintray.com/carrotindustries/horizon-eda-focal horizon-eda-focal main
```

As these packages are signed with Bintray's GPG key, you'll have to add it to apt's keyring:
```
curl https://bintray.com/user/downloadSubjectPublicKey?username=bintray | sudo apt-key add -
```

When installing you might need to specify the release to get the version from Bintray rather than the one provided by your distribution:
```
apt-get install -t horizon-eda-buster horizon-eda
```

The debian packaging files located in `debian` are derived from the [Debian-maintained package](https://packages.debian.org/sid/horizon-eda).
Compared to the Debian-maintained package, this package omits:

 - Doxygen-generated documentation
 - READMEs in `/usr/share/doc`
 - The python module
