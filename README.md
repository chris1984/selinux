SELinux
=======

Configures SELinux.

Requirements
------------

This role requires Ansible 2.0 or higher.

Role Variables
--------------

| Name           | Default    | Description                                       |
|----------------|------------|---------------------------------------------------|
| selinux_policy | targeted   | SELinux policy type (targeted or mls)             |
| selinux_state  | permissive | SELinux state (permissive, enforcing or disabled) |

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

Chris Roberts
