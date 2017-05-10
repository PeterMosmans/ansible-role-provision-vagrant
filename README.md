Ansible Role: provision-vagrant
===================


Build status for this role: [![Build Status](https://travis-ci.org/PeterMosmans/ansible-role-provision-vagrant.svg)](https://travis-ci.org/PeterMosmans/ansible-role-provision-vagrant)


This role provisions a machine for Vagrant usage. It will add the vagrant user, enable (passwordless) sudo access, and allows access with a public SSH key.


Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values.

**vagrant_key**: The public key for the vagrant user. If not specified, defaults to the default Vagrant insecure public key (as specified in `vars/main.yml`).


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

Note that a private key for the vagrant user will be added as well, which can be found under `files/id_rsa`. By default, this is the 'insecure' default private Vagrant key, to facilitate hopping to other Vagrant boxes.

License
-------

GPLv3

Author Information
------------------

Created by Peter Mosmans. Feedback always appreciated.
