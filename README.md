# Ansible role - `system_fail2ban`

Manage Fail2Ban jails and filters:
* Install or remove jails files defined in `system_fail2ban_jails` from `templates/jails`
* Install or remove filters files defined in `system_fail2ban_filters` from `templates/filters`

By default, installs the jail `sshd` and no filters.

## Tags

| Tags       | Description                           |
|------------|---------------------------------------|
| `setup`    | Install and configure Fail2Ban        |
| `teardown` | Remove Fail2Ban configuration         |
| `remove`   | Remove Fail2Ban and its configuration |

## Variables

| Variable                  | Type               | Required | Default           | Description               |
|---------------------------|--------------------|----------|-------------------|---------------------------|
| `system_fail2ban_jails`   | `list` of `string` | No       | `[sshd]`          | List of jails to manage   |
| `system_fail2ban_filters` | `list` of `string` | No       | `[]` (empty list) | List of filters to manage |

## Templates

| Template                  | Type    | Description       |
|---------------------------|---------|-------------------|
| `filters/proxmox.conf.j2` | Filters | ProxmoxVE filters |
| `jails/proxmox.conf.j2`   | Jails   | ProxmoxVE jails   |
| `jails/sshd.conf.j2`      | Jails   | SSHD jails        |
