# ansible-role-motd

Sets the login message in `/etc/motd`.

This repo holds role code only. CI comes from [ansible-pipeline](https://github.com/bunnywkwk/ansible-pipeline).

## Variables

| Variable | Default | Meaning |
| --- | --- | --- |
| `motd_message` | `Authorized users only` | Text shown at login |

## Example playbook

```yaml
- name: Login message
  hosts: all
  become: true
  roles:
    - role: motd
      vars:
        motd_message: "Lab machine"
```

## Release

Change `VERSION` in a pull request. After the merge, CI tags `v<VERSION>`.

## License

MIT
