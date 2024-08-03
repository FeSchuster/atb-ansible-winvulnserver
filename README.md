Ansible Role: atb-ansible-winvulnserver
=========

This role creates a vulnerable task and modifies the ACL of the PowerShell script executed by the task.

Requirements
------------

The vulnerability was intended for deployment within a Windows enterprise infrastructure. The privileged account carrying out the task needs the "SeBatchLogonRight" permission to run tasks as jobs.

Role Variables
--------------

``` yaml
admin_user: "wsadmin"
admin_password: "SuperSecurePW.3"
compromised_user: "Alice"
```

Dependencies
------------

pywinrm

Example Playbook
----------------

```yaml
    - hosts: vulnserver
      roles:
         - role: atb-ansible-winvulnserver
```
License
-------

MIT

Author Information
------------------

Sebahattin Sahin
