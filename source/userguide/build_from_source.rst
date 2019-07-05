Build From Source
=================

Monk OS is a distro and thus relies on many OpenSource components. The source for the OpenSource components are configured in the Yocto layers and are fetched when we build our distro. All the code for Monk OS distro are readily available in this repository and is open to edits.

Since the layer are spread across different repos and also the layers needs to be selected based on the device, we are using `repo tool <https://www.chromium.org/developers/how-tos/depottools>`_ from depot-tools.

Setting up repo tool
Clone the depot_tools repository:
.. code::

    $ git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git

Add depot_tools to the end of your PATH (you will probably want to put this in your ~/.bashrc or ~/.zshrc). Assuming you cloned depot_tools to /path/to/depot_tools:
.. code::

    $ export PATH=$PATH:/path/to/depot_tools

Fetching the Monk OS Layers
.. code::

    repo init -u https://gitlab.com/monkos/monkos-setup
    repo sync

Sourcing the Distro
The Distro is sourced using the script setup-monk:

.. code::

    source setup-monk

The branch to be build can be specified using the -b option:

.. code::

    source setup-monk -b sumo

The target device can be specified using the -d option:

.. code::

    source setup-monk -d raspberrypi

For more help on sourcing the Distro:

.. code::

    source setup-monk -help

Building the project
.. code::

    bitbake monkos-minimal-boot

Note:
Currently the development is done in sumo branch, So source the Distro for sumo branch.
