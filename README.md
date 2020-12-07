# Ansible role - `system_fail2ban`

Manage Fail2Ban.

## Tags

| Tags       | Description                           |
|------------|---------------------------------------|
| `setup`    | Install and configure Fail2Ban        |
| `teardown` | Remove Fail2Ban configuration         |
| `remove`   | Remove Fail2Ban and its configuration |

## Templates

| Template                 | Description      |
|--------------------------|------------------|
| `managed.filter.conf.j2` | Fail2Ban filters |
| `managed.filter.conf.j2` | Fail2Ban jails   |
