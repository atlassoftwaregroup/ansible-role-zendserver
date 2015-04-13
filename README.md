zendserver
==========
This Ansible role lets you install Zend Server on the specified host. This is a fork of rtuin.zendserver that installs the ssl version for Zend Server 6.3.

Requirements
------------
None


Role Variables
--------------

In the current version, you can specify the following variables:

| Name               | Default |                                                    |
|--------------------|---------|----------------------------------------------------|
| zendserver_version | 6.3     | The version of Zend Server to install              |
| php_version        | 5.5     | The version of PHP to install                      |
| php_cli_in_path    | true    | Add the Zend Server binary dir to the bash profile |


Dependencies
------------
None


License
-------
MIT

Author Information
------------------

Created by Richard Tuin
https://www.twitter.com/Richard_Tuin
http://www.rtuin.nl

Examples
--------

```
---
- name: Zend Server test
  hosts: all
  roles:
    - rtuin.zendserver
```

Or, using parameters:

```
---
- name: Zend Server test
  hosts: all
  roles:
    - { role: rtuin.zendserver, php_version: 5.4, zendserver_version: 6.2 }
```

Note
----
This fork of rtuin.zendserver adds the correct ssl version for zendserver.
