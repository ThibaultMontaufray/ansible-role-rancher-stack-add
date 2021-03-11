RANCHER ADD STACK
=================

This roles add a stack in rancher

Example Playbook
----------------

Here is a use case :

```yaml
  - hosts: servers
    remote_user: mysuperadmin
    vars:
      - rancher_api_key: "123456789ABCDEFG"
      - rancher_api_secret: "MY_SUPER_API_SECRET"
      - rancher_project_name: "servodroid"
      - rancher_project_id: "{{ rancher_pj.rancher_project_id }}"
      - stack_name: "STACK_NAME"
      - hostmaster: "{{ hostvars[groups['rancher-master'][0]]['ansible_default_ipv4']['address'] }}"
      - rancher_url: "http://{{ hostmaster }}:8080"
      - rancher_master_url: "http://{{ hostmaster }}:8080"
      - stack_project: "PROJECT_STACK_NAME"
  - roles:
     - ansible-role-rancher-add-stack
```

License
-------

MIT
