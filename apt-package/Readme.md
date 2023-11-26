# Simple Debian package

The Debian package manager is still widely used and this directory contains a very basic example how to build your Debian package. It will install a single shell script to /usr/local/bin and runs through all stages of installation/removal.

## How to use
In the folder where this readme is located run the following command, to build the package:

    dpkg --build sample-functions_1.0.0_amd64

After that you should find a file named sample-functions_1.0.0_amd64.dep in this folder and that is your build APT package. You can now install/remove this package with:

    sudo dpkg -i ./sample-functions_1.0.0_amd64.deb 
    sudo dpkg -r sample-functions