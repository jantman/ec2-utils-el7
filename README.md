ec2-utils-el7
==============

[![Project Status: Unsupported – The project has reached a stable, usable state but the author(s) have ceased all work on it. A new maintainer may be desired.](http://www.repostatus.org/badges/latest/unsupported.svg)](http://www.repostatus.org/#unsupported)

**Deprecated / Unsupported** - Now that [Amazon Linux 2 is out](https://aws.amazon.com/about-aws/whats-new/2017/12/introducing-amazon-linux-2/) and uses systemd, it should be possible to use those packages on EL7. Hopefully.

Amazon Linux ships with an ``ec2-utils`` package that contains some Apache2-licensed
scripts for dealing with EC2 networking, such as automatically detecting and adding
additional interfaces.

Amazon Linux is based on CentOS 6 which uses [upstart](http://upstart.ubuntu.com/)
as its init subsystem. This is unfortunate for anyone running EL7-based systems
in AWS, as it uses [systemd](http://www.freedesktop.org/wiki/Software/systemd/).

This repository repackages Amazon's ``ec2-utils`` for EL7, with the relevant
upstart scripts converted to systemd units.

