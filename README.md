ec2-utils-el7
==============

Amazon Linux ships with an ``ec2-utils`` package that contains some Apache2-licensed
scripts for dealing with EC2 networking, such as automatically detecting and adding
additional interfaces.

Amazon Linux is based on CentOS 6 which uses [upstart](http://upstart.ubuntu.com/)
as its init subsystem. This is unfortunate for anyone running EL7-based systems
in AWS, as it uses [systemd](http://www.freedesktop.org/wiki/Software/systemd/).

This repository repackages Amazon's ``ec2-utils`` for EL7, with the relevant
upstart scripts converted to systemd units.
