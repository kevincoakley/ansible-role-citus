ansible-role-citus
==================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-citus.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-citus)

Install Postgresql Citus Community Edition (single machine and clustered) - https://www.citusdata.com/ . Tested with Citus 7.2 on CentOS 7.

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml and the example inventory below

Dependencies
------------

None

Example Playbook
----------------

    - name: Install the Citus role for CentOS
      hosts: citus
      become: yes
      become_method: sudo
       
      roles:
        - ansible-role-citus
    
      tags:
        - citus

Example Inventory
-----------------
   
    [citus]
    centos-system-1 citus_coordinator=True
    centos-system-2 citus_coordinator=False
    centos-system-3 citus_coordinator=False
    

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)