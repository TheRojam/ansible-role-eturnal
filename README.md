eturnal debian
==============

[![Build Status](https://app.travis-ci.com/therojam/ansible-role-eturnal.svg?branch=main)](https://travis-ci.com/therojam/ansible-role-eturnal) 
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-eturnal-blue.svg)](https://galaxy.ansible.com/therojam/ansible_role_eturnal)

This roles is for setting up eturnal a new stun/turn server.

More information on [github.com processone/eturnal](https://github.com/processone/eturnal).


Requirements
------------

Installed debian server.

Role Variables
--------------

defaults/main.yml:

```
eturnal_secret: "r4nd0m_s|_|p3r+10nG"               # Shared secret 
eturnal_ipv4: "{{ ansible_default_ipv4.address }}" # The server's public IPv4 address.
eturnal_ipv6: "{{ ansible_default_ipv6.address }}" # The server's public IPv6 address (optional).
```

Remember to may change the `etunral_sceret` in your variables definition to your own shared secret.
The `eturnal_ipv4` (and `eturnal_ipv6`) should be your public ip address(es). After running your playbook, please check that your `/etc/eturnal/eturnal.yml` definitions matches with your public ip addresses.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: therojam.ansible_role_eturnal }

License
-------

BSD

Author Information
------------------
Role was written by:

* therojam <github@therojam.tech> 

