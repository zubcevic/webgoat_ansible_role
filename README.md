webgoat_ansible_role
=========

[![Build Status](https://travis-ci.org/zubcevic/webgoat_ansible_role.svg)](https://travis-ci.org/zubcevic/webgoat_ansible_role)

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

Java can be installed using variables. See [WebGoat role blog](https://zubcevicdotcom.wordpress.com/owasp-webgoat/deploying-webgoat-using-ansible/).


Role Variables
--------------

There are no mandatory variables.

Dependencies
------------

For the **native** install make sure you have Java installed or install it with the use of variables. See tests/localsecure.yml 
For the **docker** install supply the **webgoat_installtype** variable with value **docker** and have docker installed and on the ansible host make sure you have docker-py installed. 
    
Example Playbook
----------------

Here is an example for installing WebGoat, using a playbook (webgoat-playbook.yaml) with the following content:

    - hosts: servers
      roles:
         - role: zubcevic.webgoat_ansible_role

From commandline:
         
    ansible-playbook webgoat-playbook.yaml

or:

    ansible-playbook -e "webgoat_installtype=docker" webgoat-playbook.yaml
    
Example with JRE 11 local java installation and HTTPS for webgoat:

	ansible-playbook -c local tests/localsecure.yml
	

License
-------

MIT

Author Information
------------------

[René Zubcevic](https://github.com/zubcevic)
