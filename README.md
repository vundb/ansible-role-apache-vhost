Ansible Role Apache Vhost
======================================

Ansible role to manage apache's virtual hosts on gentoo instances.

Supported Distributions
-----------------------

- Gentoo

Role Variables
--------------

- `apache_services`:
Array with services to be restarted on configuration changes.

- `apache_user`:
System user name for apache daemon. Default value is `apache`.

- `apache_group`:
System user group for apache daemon. Default value is `apache`.

- `apache_vhosts`:
Array with virtual host configuration. See
[default vars file](defaults/main.yml)

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: vundb-apache-vhost
      apache_vhosts:
       - label:         "example.com"
         virtual_host:  "*:80"
         server_name:   "example.com"
         server_alias:  "example.com"
         document_root: "/var/www/example.com"
```

License
-------

MIT

Author Information
------------------

- You can find more roles in my GitHub channel [vundb](https://github.com/vundb)
- Follow me on Twitter [@vundb](https://twitter.com/vundb)
