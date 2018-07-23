==============================
ssato.opentlc_workstation
==============================

ssato.opentlc_workstation is an ansible role to setup workstaion used to be
named as bastion host in environments provided by OpenTLC [#]_.

Requirements
==============

Software
----------

- python >= 2.6
- pexpect >= 3.3

Dependencies
--------------

- Apparently, bastion host provided by OpenTLC is needed.

Example Playbook
==================

::

  - hosts: bastion
    vars:
      opentlc_username: foo-example.com
      opentlc_bastion_short_hostname: bastion
      opentlc_guid: xyz0
    roles:
      - role: ssato.opentlc_workstation

License
===========

MIT

Author
==========

Satoru SATOH [ssato@Github](https://github.com/ssato)

.. [#] https://labs.opentlc.com

.. vim:sw=2:ts=2:et:
