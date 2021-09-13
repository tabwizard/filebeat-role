Filebeat Role
=========

Устанавливает и настраивает Filebeat

Requirements
------------

Поддерживаются только ОС семейств debian и EL.

Role Variables
--------------

|   Variable name   |   Default   |   Description                                                      |
|-------------------|-------------|--------------------------------------------------------------------|
| filebeat_version  | "7.14.1"    | Параметр, который определяет какой версии kibana будет установлена |
| kibana_instance   | "{{ hostvars['kbn-instance']['ansible_facts']['default_ipv4']['address'] }}" | Адрес хоста Kibana                                                 |
| elastic_instance  | "{{ hostvars['el-instance']['ansible_facts']['default_ipv4']['address'] }}" | Адрес хоста с Elasticsearch                                        |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- name: Install Filebeat
  hosts: servers
  roles:
    - role: filebeat-role
      vars:
        elastic-instance: 1.2.3.4
        kibana_instance: 1.2.3.5
```

License
-------

MIT

Author Information
------------------

Andrey Pirozhkov tabwizard@gmail.com.
