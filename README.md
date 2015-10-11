# Users and Groups Management



## Usage

Playbook and vars files

```YAML
- name: My Plaubook
  hosts: "{{ hosts }}"

  var_files:
    - ../vars/common_configs.yml

  roles:
    - users_and_groups
```

`vars/common_configs.yml` or `group_vars/production.yml` or `hosts/my_host`

```YAML
users_and_groups:
  groups:
    - admins
    - view_logs
  users:
    - name: wojtek.oledzki
      ssh_key_file: files/ssh_keys/wojtek.oledzki.pub
      groups:
        - view_logs
```




## License

The MIT License (MIT)  
Copyright (c) 2015 Voytek Solutions LTD
