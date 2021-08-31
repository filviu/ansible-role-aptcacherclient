# Ansible Role: AptCacherNg client setup

[![CI](https://github.com/silviuvulcan/ansible-role-aptcacherclient/workflows/CI/badge.svg?event=push)](https://github.com/silviuvulcan/ansible-role-aptcacherclient/actions?query=workflow%3ACI)

Sets up a Debian/Ubuntu/Proxmox/Rasbian machine to use a apt-cacher-ng for apt updates. Also a small helper script that allows apt to work when the cache server is down

## Requirements

None.

## Role Variables

See `defaults/main.yml` for examples.

    aptcacher_servers:
      - "example.com:3142"

    aptcacher_detect_script_path: "/usr/local/bin"

Path where to deploy the helper script

    aptcacher_show_proxy_messages: true

Whether to show some messages from the proxy when running apt

## Dependencies

This role needs the netcat package (and it will install it).

## Example Playbook

```yaml
---
- hosts: all

roles:
      - silviuvulcan.aptcacherclient
          aptcacher_servers:
            - "apt-cache:3142"
          aptcacher_detect_script_path: "/usr/local/bin"
        aptcacher_show_proxy_messages: true
```

## License

MIT / BSD


## Author Information

This role was created by Silviu Vulcan to scratch his own itch.
