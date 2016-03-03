# django-vagrant-provisioner

**A vagrant provisioner that sets up a Ubuntu14.04 along with mysql, virtualEnv and all required pip packages to get up & running with django development.**

This vagrant box was necessary for development purposes because setting up django environment on Mac OSX with MySQL configs etc were proving to be challenging. So I wanted to create a ubuntu virtualbox which would have everything readymade in it out-of-the-box

Open your terminal. Clone this repo. `cd` to the repo's root folder. And then, type `vagrant up`.

All necessary ubuntu packages will be updated, mysql installed and configured with `root:root` credenetials, python virtualenv installed, pip packages installed along with easy verbose messages. Should be easy to go forward with django development from there onwards.

View the `vg-provisioner` file to learn how all the magic happens in creating the vagrant box
