Requirements
============

* An rpi or equivalent device like beaglebone / odroid which you are planning to run as your router/firewall for internet

* rpi / beaglebone comes with only one ethernet interface. Unless you are planning to use USB wifi adapter, you would need USB Ethernet adapter to connect your external access point (which I strongly recommend for wifi range and performance)

* To run this setup, you need a fresh installation of rpi with rasbian (or any other debian based OS), which you can connect via ssh in your network

* The workstation (the computer from which you are going to configure your router) needs `ansible` to be installed.



Setup
=====

`git clone https://github.com/selvakn/pi.router.git && cd pi.router`

`cp group_vars/all.yml.sample group_vars/all.yml`
\# It has sane defaults, but you should modify it to suite your needs.

\# Modify `hosts` file to point to your rpi or equivalent device

`ansible-galaxy install -r requirements.yml`

Once installation is complete, connect your workstation to your `internal_interface` of your rpi and you should be assigned DHCP ip in the configured range!


If you have idea / thoughts, pull requests, issues are welcome!
