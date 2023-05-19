# ansiblie-role-aci-tenant
Custom Infrastructure-as-Code ACI Tenant Role for logical configuration under Tenant tab in APIC GUI

Use the following in the collection requirements.yml file

https://galaxy.ansible.com/docs/using/installing.html

```yaml
---
roles:
  - name: aci-tenant
    src: https://github.com/cisco-apjc-cloud-se/ansiblie-role-aci-tenant
    version: main
    scm: git
```

Execute the role as a play with host/inventory and customised variables (intent.yml and encrypted_password.yml)

```yaml
- name: Execute ACI Tenant Role
  hosts: apic
  # connection: local
  gather_facts: false
  vars_files:
    - encrypted_password.yml
    - intent.yml
  vars:
    output_path: config.json
    output_level: debug
    timeout: 120
    validate_certs: false
  roles:
    - role: aci-tenant
```