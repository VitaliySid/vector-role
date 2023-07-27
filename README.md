vector-role
=========

The role installs and configures the `vector` application   
Supported and tested operating system `Centos 7`

Role Variables
--------------
- `clickhouse_url` - ip-address API `clickhouse` 
- `vector_version` - version of the application being installed
- `clickhouse_user` - user login db `clickhouse` 
- `clickhouse_password` - user password db `clickhouse` 

```yml

clickhouse_url: http://192.168.56.10:8123
vector_version: "0.31.0-1"
clickhouse_user: "{{api_user}}"
clickhouse_password: "{{api_password}}"
```

Example Playbook
----------------

```yml

- hosts: vector
  tags: [vector]
  roles:
    - vector-role
```

License
-------

BSD


