Role Name
=========

Sets up basic detection of a apt-cacher client

Role Variables
--------------

Check defaults/main for variables that can be adjusted

Dependencies
------------

This doesn't make sense if you don't run an apt cacher instance somewhere

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - hosts: all

      roles:
        - { role: silviuvulcan.apt_cacher_client, when: ansible_os_family == 'Debian' }


License
-------

BSD


Author Information
------------------

https://github.com/silviuvulcan/ansible-role-aptcacherclient/
