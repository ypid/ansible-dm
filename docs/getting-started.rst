Getting started
===============

.. include:: includes/all.rst

.. contents::
   :local:


Example inventory
-----------------

To manage the display manager on a given host it should be included in the
``debops_service_dm`` Ansible inventory group:

.. code:: ini

   [debops_service_dm]
   hostname

Example playbook
----------------

If you are using this role without DebOps, here's an example Ansible playbook
that uses the ``ypid.dm`` role:

.. literalinclude:: playbooks/dm.yml
   :language: yaml

This playbooks is shipped with this role under :file:`./docs/playbooks/dm.yml`
from which you can symlink it to your playbook directory.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after a host was first
configured to speed up playbook execution, when you are sure that most of the
configuration is already in the desired state.

Available role tags:

``role::dm``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::dm:pkg``
  Tasks related to system package management like installing or
  removing packages.
