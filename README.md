basic-network
=============

[![Build Status](https://travis-ci.org/cognifloyd/ansible-role-basic-network.svg?branch=master)](https://travis-ci.org/cognifloyd/ansible-role-basic-network)

Remove Redhat's persistent device names and setup basic eth0 device that uses dhcp.
This is perfect for VMs, especially vagrant boxes.

Requirements
------------

This is RedHat/CentOS specific. The kernel should be booted with net.ifnames=0 biosdevnames=0, but I haven't added a task for that yet.

Role Variables
--------------

no vars

Dependencies
------------

no deps. Maybe there will be a dep to change grub's cmdline, but not yet.

Example Playbook
----------------

    - hosts: all
      roles:
         - cognifloyd.basic-network

License
-------

MIT

Author Information
------------------

By Jacob Floyd (@cognifloyd) while working for Theatro Labs, Inc. (theatro.com). Adapted from [centos7.ks](https://github.com/CentOS/sig-cloud-instance-build/blob/5162d86c/vagrant/centos7.ks) and [geerlingguy.packer-rhel](https://galaxy.ansible.com/geerlingguy/packer-rhel/).
