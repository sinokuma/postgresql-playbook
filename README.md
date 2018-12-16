PostgreSQL Playbook
=========

PostgreSQL 11 Installation for Linux

Requirements
------------

In order to use PostgreSQL module, psycopg2 is necessary.
Please install psycopg2 before using PostgreSQL module.

Role Variables
--------------

The default value of PostgreSQL is defined in `defaults/main.yml`.
If overwriting, please define it in `vars/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

Inside `site.yml`:

```yml
---
- hosts: postgresql-server
  roles:
    - postgresql

```

Inside `inventory/hosts.yml`:

```yml
---
postgresql-server:
  hosts:
    localhost:
  vars:
    ansible_port: 10022
    ansible_user: root

```

License
-------

BSD

Author Information
------------------

None.
