flatpak_update
==============
[![Ansible Lint](https://github.com/oxivanisher/role-flatpak_update/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-flatpak_update/actions/workflows/ansible-lint.yml)

This role updates all flatpak packages and runtimes to the latest version. This is a very dirty role and not perfectly idempotent. Please point your frustration about this to the flatpak developers.
It will only run if the flatpak command is available on the system.

Role Variables
--------------

| Name                            | Comment                                                            | Default value  |
|---------------------------------|--------------------------------------------------------------------|----------------|
| flatpak_update_user             | The user for which the flatpak update command is run.              | `root`         |

Example Playbook
----------------
```yaml
- name: Update all flatpak packages
  hosts: client
  collections:
    - oxivanisher.flatpak_update
  roles:
    - role: oxivanisher.linux_desktop.flatpak_update
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_desktop](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_desktop/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_desktop).
