# Ansible Role - systemd

Ansible role for systemd

## Install role via `roles/requirements.yml`

### Read-Only copy

Configure the role as read-only copy:

```yml
---
# systemd
- src: https://github.com/dreknix/ansible-role-systemd.git
  scm: git
  version: main
  name: systemd
...
```

Install the role:

```console
$ ansible-galaxy role install --force -r roles/requirements.yml
```

### Working copy

Configure the role as a working copy:

```yml
---
# systemd
- src: git@github.com:dreknix/ansible-role-systemd.git
  scm: git
  version: main
  name: systemd
...
```

Install the working copy:

```console
$ ansible-galaxy role install --force --keep-scm-meta -r roles/requirements.yml
```

## Using in a Playbook

This role is only used for reloading the systemd daemon. A task calls the
handler via `notify: systemd_reload_systemd`.

## License

[MIT](https://github.com/dreknix/ansible-role-systemd/blob/main/LICENSE)
