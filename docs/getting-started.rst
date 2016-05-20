Getting started
===============

.. contents::
   :local:


Example inventory
-----------------

To configure GDM on host given in ``ypid_service_gdm`` Ansible inventory group:

.. code:: ini

    [ypid_service_gdm]
    hostname

Example playbook
----------------

Here's an example playbook that can be used to manage GDM::

    ---
    - name: Configure the GNOME Display Manager.
      hosts: [ 'ypid_service_gdm' ]
      become: True

      roles:

        - role: ypid.gdm
          tags: [ 'role::gdm' ]


Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::gdm``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.
