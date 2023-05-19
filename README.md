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