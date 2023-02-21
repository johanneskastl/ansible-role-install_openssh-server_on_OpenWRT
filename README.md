install_openssh-server_on_OpenWRT
=========

Install the OpenSSH server on OpenWRT

Requirements
------------

Note for provisioning an OpenWRT instance using the `root` user:

You must have configured PubKeyAuthentication on the dropbear instance, running on OpenWRT by default. This role will re-use the `authorized_keys` file from dropbear and put it into the `ansible_user`s home directory, so passwordless logins are still working with the OpenSSH Server.

This role includes a safeguard and will abort, if you are connecting as `root` user and there is no `authorized_keys` file.

Role Variables
--------------

None.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.install_openssh-server_on_OpenWRT'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
