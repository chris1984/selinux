SELinux
=======

Configures SELinux on hosts.

[![Build Status](https://travis-ci.org/chris1984/selinux.svg?branch=master)](https://travis-ci.org/chris1984/selinux)

Requirements
------------

This role requires Ansible 2.0 or higher.

Role Variables
--------------

* Variables are all in role/defaults/main.yml

```markdown
| Name           | Default    | Description                                       |
|----------------|------------|---------------------------------------------------|
| selinux_policy | targeted   | SELinux policy type (targeted or mls)             |
| selinux_state  | permissive | SELinux state (permissive, enforcing or disabled) |
```

Dependencies
------------

None

Example Playbook
----------------

Configure SELinux in permissive mode.

```yaml
- hosts: all
  roles:
    - { role: chris1984.selinux }
```

Disable SELinux

```yaml
- hosts: all
  roles:
    - { role: chris1984.selinux, selinux_state: disabled }
```

Configure SELinux to use mls policy and enforcing mode

```yaml
- hosts: all
  roles:
    - { role: chris1984.selinux, selinux_policy: mls, selinux_state: enforcing}
```

License
-------

MIT

Author Information
------------------

* Chris Roberts - chrobert@redhat.com  - https://www.linkedin.com/in/croberts84/
* Work at Redhat on the Foreman/Katello projects and also maintain fog-vsphere.
