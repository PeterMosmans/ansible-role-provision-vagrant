Ansible Role: http2
===================


Build status for this role: [![Build Status](https://travis-ci.org/PeterMosmans/ansible-role-provision-vagrant.svg)](https://travis-ci.org/PeterMosmans/ansible-role-provision-vagrant)


This role provisions a machine for Vagrant usage. It will add the vagrant user, enable sudo access, and copy the (insecure) default SSH key to the machine.


Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - role: PeterMosmans.provision-vagrant
```



License
-------

GPLv3

Author Information
------------------

Created by Peter Mosmans. Feedback always appreciated.
