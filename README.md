# [lvm](#lvm)

Configure Logical Volumes Management (lvm), group and volumes.

|GitHub|GitLab|Quality|Downloads|Version|
|------|------|-------|---------|-------|
|[![github](https://github.com/robertdebock/ansible-role-lvm/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-lvm/actions)|[![gitlab](https://gitlab.com/robertdebock/ansible-role-lvm/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-lvm)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/robertdebock/lvm)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/robertdebock/lvm)|[![Version](https://img.shields.io/github/release/robertdebock/ansible-role-lvm.svg)](https://github.com/robertdebock/ansible-role-lvm/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/resources/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: robertdebock.lvm
```

The machine needs to be prepared in CI this is done using `molecule/resources/prepare.yml`:
```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: robertdebock.bootstrap
```

Also see a [full explanation and example](https://robertdebock.nl/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for lvm

# Per lvm a size can be set, if it's not set, use this value.
lvm_default_pesize: 32

# A list of volume groups.
# lvm_volume_groups:
#   - name: first
#     pvs:
#       - /dev/sdb1
#   - name: second
#     pvs:
#       - /dev/sdb2
#     pesize: 128K
#   - name: third
#     pvs:
#       - /dev/sdb3
#       - /dev/sdb4

# A list of volumes.
# lvm_logical_volumes:
#   - name: first
#     vg: first
#     size: 512
#     opts:
#       - --type cache-pool
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/robertdebock/ansible-role-lvm/blob/master/requirements.txt).

## [Status of requirements](#status-of-requirements)

The following roles are used to prepare a system. You may choose to prepare your system in another way, I have tested these roles as well.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
| [robertdebock.bootstrap](https://galaxy.ansible.com/robertdebock/bootstrap) | [![Build Status GitHub](https://github.com/robertdebock/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-bootstrap/actions) | [![Build Status GitLab ](https://gitlab.com/robertdebock/ansible-role-ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/robertdebock/ansible-role-bootstrap)

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/ansible-role-lvm/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|alpine|all|
|amazon|all|
|debian|all|
|el|7, 8|
|fedora|all|
|opensuse|all|
|ubuntu|focal, bionic|

The minimum version of Ansible required is 2.9, tests have been done to:

- The previous version.
- The current version.
- The development version.



If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-lvm/issues)

## [License](#license)

Apache-2.0

## [Contributors](#contributors)

I'd like to thank everybody that made contributions to this repository. It motivates me, improves the code and is just fun to collaborate.


## [Author Information](#author-information)

[Robert de Bock](https://robertdebock.nl/)

Please consider [sponsoring me](https://github.com/sponsors/robertdebock).
