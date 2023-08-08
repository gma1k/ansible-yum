# ansible-yum
Ansible role for yum.

* Role Variables
* Default Role Variables
* Package variables


# Service variables

```
yum_upgrade_now_first_boot_file     : "/var/local/ansible_yum_upgrade"
```
# Main configuration

```
yum_default_packages                : ""
yum_upgrade_now_force               : False
yum_reboot_if_needed                : True
yum_upgrade_now_pause_after_reboot  : 5
yum_upgrade_now_ssh_port            : "{{ ansible_port | default(22) }}"
```

## Example playbook 

```
- hosts: servers
  roles:
    - { role: ansible-yum }
```
