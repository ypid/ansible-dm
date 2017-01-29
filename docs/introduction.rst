Introduction
============

Configure a display manage. Supported options are:

* `GNOME Display Manager <https://en.wikipedia.org/wiki/GNOME_Display_Manager>`_.
* `LightDM <https://en.wikipedia.org/wiki/LightDM>`_.


Installation
~~~~~~~~~~~~

This role requires at least Ansible ``v2.1.4``. To install it, run::

    ansible-galaxy install ypid.dm


This role uses features recently introduced in Jinja2, namely
the ``equalto`` filter which was released with
`Jinja 2.8 <http://jinja.pocoo.org/docs/dev/changelog/#version-2-8>`__.
Jinja 2.8 is `available in Debian Jessie Backports <https://packages.debian.org/search?keywords=python-jinja2>`__.

..
 Local Variables:
 mode: rst
 ispell-local-dictionary: "american"
 End:
