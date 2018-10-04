cargo
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-cargo.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-cargo)

Provides cargo for your system.

[Unit tests](https://travis-ci.org/robertdebock/ansible-role-cargo) are done on every commit and periodically.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-cargo/issues)

To test this role locally please use [Molecule](https://github.com/metacloud/molecule):
```
pip install molecule
molecule test --scenario-name fedora-latest
```
There are many scenarios available, please have a look in the `molecule/` directory.

Context
-------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/cargo.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.

Role Variables
--------------

None known.

Dependencies
------------

This role can be used to prepare your system:

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)
- [robertdebock.epel](https://travis-ci.org/robertdebock/ansible-role-epel)
- [robertdebock.buildtools](https://travis-ci.org/robertdebock/ansible-role-buildtools)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|ansible 2.7|ansible devel|
|------------|-----------|-----------|-----------|-----------|-------------|
|alpine-edge|yes|yes|yes|yes|yes|
|alpine-latest|yes|yes|yes|yes|yes|
|archlinux|yes|yes|yes|yes|yes|
|centos-6|no|no|no|no|no|
|centos-latest|yes|yes|yes|yes|yes|
|debian-latest|yes|yes|yes|yes|yes|
|debian-stable|yes|yes|yes|yes|yes|
|fedora-latest|yes|yes|yes|yes|yes|
|fedora-rawhide|yes|yes|yes|yes|yes|
|opensuse-leap|yes|yes|yes|yes|yes|
|opensuse-tumbleweed|yes|yes|yes|yes|yes|
|ubuntu-artful|yes|yes|yes|yes|yes|
|ubuntu-latest|yes|yes|yes|yes|yes|

Example Playbook
----------------

The simplest way possible:
```
- hosts: servers

  roles:
    - robertdebock.bootstrap
    - robertdebock.buildtools
    - robertdebock.cargo
```

Install this role using `galaxy install robertdebock.cargo`.

License
-------

Apache License, Version 2.0

Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
