webgoat-ansible-role
=========

[![Build Status](https://travis-ci.org/zubcevic/webgoat-ansible-role.svg)](https://travis-ci.org/zubcevic/webgoat-ansible-role)

The **webgoat** role for Ansible let's you install and run WebGoat. You can choose a native install based on an available Java runtime or a Docker based install. 
**The role is still under development**

Requirements
------------

A host with Linux on it and either a Java Runtime or a Docker runtime.

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
         - role: webgoat-ansible-role
         
    ansible-playbook -t native webgoat-playbook.yaml

License
-------

TBD.

Author Information
------------------

René Zubcevic
