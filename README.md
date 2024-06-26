# Ansible role [code](https://galaxy.ansible.com/ui/standalone/roles/buluma/code/documentation)

Install visual studio code on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-code/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-code/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-code.svg)](https://github.com/buluma/ansible-role-code/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-code.svg)](https://github.com/buluma/ansible-role-code/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-code.svg)](https://github.com/buluma/ansible-role-code/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/code)](https://galaxy.ansible.com/ui/standalone/roles/buluma/code/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-code/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  pre_tasks:
    - name: Update apt cache.
      apt: update_cache=true cache_valid_time=600
      when: ansible_os_family == 'Debian'

  roles:
    - role: buluma.ca_certificates
    - role: buluma.microsoft_repository_keys
    - role: buluma.code
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-code/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.


## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-code/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.ca_certificates](https://galaxy.ansible.com/buluma/ca_certificates)|[![Ansible Molecule](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-ca_certificates.svg)](https://github.com/shadowwalker/ansible-role-ca_certificates)|
|[buluma.microsoft_repository_keys](https://galaxy.ansible.com/buluma/microsoft_repository_keys)|[![Ansible Molecule](https://github.com/buluma/ansible-role-microsoft_repository_keys/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-microsoft_repository_keys/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-microsoft_repository_keys.svg)](https://github.com/shadowwalker/ansible-role-microsoft_repository_keys)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-code/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/r/buluma/debian)|all|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|39, 38|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|focal, bionic, jammy|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-code/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-code/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-code/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
