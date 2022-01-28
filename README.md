eturnal debian
==============

[![Build Status](https://api.travis-ci.com/therojam/ansible-role-eturnal.svg?branch=master)](https://travis-ci.org/therojam/ansible-role-eturnal) 
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-eturnal-blue.svg)](https://galaxy.ansible.com/therojam/eturnal)

This roles is for setting up eturnal a new stun/tunr server.

More information on [github.com processone/eturnal](https://github.com/processone/eturnal).


Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

defaults/main.yml:
``
eturnal_secret: "r4nd0m_s|_|p3r+10nG"               # Shared secret 
eturnal_ipv4: "{{ ansible_default_ipv4.address }}" # The server's public IPv4 address.
eturnal_ipv6: "{{ ansible_default_ipv6.address }}" # The server's public IPv6 address (optional).

``
Remember to may change the `etunral_sceret` in your variables defintion to your own shared secret.
The `eturnal_ipv4` (and `eturnal_ipv6`) should be your public ip address(es). After running your playbook, please check that your `/etc/eturnal/eturnal.yml` defintions matches with your public ip adresses.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------
Role was written by:

* therojam <github@therojam.tech> 

