Chef Elements
===============

This folder contains necessary DIB elements to build Chef image
expected by "Orion Chef" Murano application.


Prerequisites
-------------

1. Install diskimage-builder

.. sourcecode:: bash

    sudo pip install diskimage-builder

2. Install qemu-utils and kpartx


On Ubuntu, Debian:

.. sourcecode:: bash

    sudo apt-get install qemu-utils kpartx

On Centos, Fedora:

.. sourcecode:: bash

    sudo yum install qemu-utils kpartx


Image building
--------------

.. sourcecode:: bash

    sudo ELEMENTS_PATH=${murano_agent_root}/contrib/elements:${murano_apps_root}/Chef/OrionChef/elements disk-image-create \
        vm ubuntu murano-agent chef -o ubuntu14.04-x64-chef

Where ${murano_agent_root} is a path to murano-agent files
and ${murano_apps_root} is a path to murano-apps files.
