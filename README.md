# devpi-upstart
Upstart script and instructions to get a permanent devpi daemon up and running

# Installation
Installation is via pip. See [here](http://doc.devpi.net/0.9.2/quickstart-server.html) for more detailed instructions

    sudo pip install devpi-server

Add a group for running devpi, we don't want to run as root.

    sudo adduser --system --home /var/cache/devpi --shell /bin/false devpi

Now download the upstart script and away you go!

    cd /etc/init && sudo curl -O https://raw.githubusercontent.com/dwurf/devpi-upstart/master/devpi.conf
    sudo service devpi start
    sudo pip install -i http://localhost:3141/root/pypi/+simple/ simplejson
