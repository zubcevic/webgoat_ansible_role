webgoat-ansible-role
=========

[![Build Status](https://travis-ci.org/zubcevic/webgoat-ansible-role.svg)](https://travis-ci.org/zubcevic/webgoat-ansible-role)

The **webgoat** role for Ansible let's you install and run WebGoat. You can choose a native install based on an available Java runtime or a Docker based install. 
**The role is still under development**

Requirements
------------

A host with Linux on it and either a Java Runtime or a Docker runtime.

+ Native install
    + Java 11+
    + Free ports: 8080, 9090, 9001
+ Docker install
    + Free ports: 8080, 9090

Role Variables
--------------

There are no mandatory variables.

Dependencies
------------

For the **native** install make sure you have Java installed with e.g. 
    
    ansible-galaxy install lean_delivery.java

Example Playbook
----------------

Here is an example for installing WebGoat, using a playbook (webgoat-playbook.yaml) with the following content:

    - hosts: servers
      roles:
         - role: zubcevic.webgoat-ansible-role

From commandline:
         
    ansible-playbook webgoat-playbook.yaml

or:

    ansible-playbook -e "webgoat_installtype=docker" webgoat-playbook.yaml

License
-------

MIT

Author Information
------------------

[René Zubcevic](https://github.com/zubcevic)
