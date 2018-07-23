==============================
ssato.opentlc_workstation
==============================

ssato.opentlc_workstation is an ansible role to setup workstaion used to be
named as bastion host in environments provided by OpenTLC [#]_.

.. image:: https://img.shields.io/travis/ssato/ansible-role-opentlc_workstation
   :target: https://travis-ci.org/ssato/ansible-role-opentlc_workstation
   :alt: [Test status]

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
      # These are MUST.
      opentlc_username: foo-example.com
      opentlc_bastion_short_hostname: bastion
      opentlc_guid: xyz0

      # These are optional
      # opentlc_ssh_identity_file: /home/foo/id_rsa_opentlc
      # opentlc_domain: example.opentlc.com
      # install_packages:
      #   - zsh
      #   - tmux
      #   - ansible
    roles:
      - role: ssato.opentlc_workstation

License
===========

MIT

Author
==========

Satoru SATOH `ssato@Github <https://github.com/ssato>`_

.. [#] https://labs.opentlc.com

.. vim:sw=2:ts=2:et:
