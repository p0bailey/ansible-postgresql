Postgresql
=========

This role install Postgresql 9.4 on top of CentOS 6.*.


Requirements
------------

N/A

Role Variables
--------------

```
postgresql_version: 9.4
# vars to create a DB,user and password.
```

The variables should be changed accordingly.

```
dbname: vagrant #change this!
dbuser: vagrant #change this!
dbpassword: vagrant #change this to a strong one!
```

##Authorized subnet or IP; in case of single IP use /32 notation.

```
auth_ip: 192.168.56.0/24
```

##Defaults

```
postgres_home: /var/lib/pgsql/
postgres_user: postgres
postgres_group: postgres
```


Dependencies
------------

N/A


Example Playbook
----------------

```
hosts: all

vars:
    postgresql_version: 9.4
    # vars to create a DB,user and password.
    dbname: vagrant #change this!
    dbuser: vagrant #change this!
    dbpassword: vagrant #change this!
    #Authorized subnet or IP; in case of single IP use /32 notation.
    auth_ip: 192.168.56.0/24
    #Defaults
    postgres_home: /var/lib/pgsql/
    postgres_user: postgres
    postgres_group: postgres

roles:
  - { role: postgresql }
```


License
-------



Author Information
------------------

Phillip Bailey phillip@bailey.st
