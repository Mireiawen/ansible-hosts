[![Build Status](https://travis-ci.com/Mireiawen/ansible-role-hosts.svg?branch=master)](https://travis-ci.com/Mireiawen/ansible-role-hosts) [![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-mireiawen.mosh-blueviolet)](https://galaxy.ansible.com/mireiawen/hosts)

# Ansible hosts

Setup entries in hosts file (/etc/hosts)


## Requirements

Access to edit the `/etc/hosts` file.

## Role Variables

### hosts_entries
The actual entries block to add to the hosts file. For example:

```
hosts_entries: |
    192.168.1.2 demo-host.localdomain
    10.11.12.13 example-database.domain.tld
```

### hosts_file
The hosts file to modify. Defaults to `/etc/hosts`

## Dependencies

None.

## Example Playbook

```
- hosts: "servers"
  roles:
  - role: "mireiawen.hosts"
    hosts_entries: |
      8.8.8.8 google.dns example.org
      192.168.0.200   example.local
```

## License
MIT, see `LICENSE`
