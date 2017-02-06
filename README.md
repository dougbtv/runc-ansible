runc-ansible
============

An ansible role to install [runc](https://runc.io/) on CentOS (primarily, for now.) 

`runc` will be installed to `/usr/local/sbin/runc` on your system, as per the runc readme.

This role is available via ansible galaxy, and can be installed with:

```
ansible-galaxy install dougbtv.runc-ansible
```

Requirements
------------

Ansible required on client machine, CentOS on target machine(s).

Role Variables
--------------

* `runc_version`: Defaults to `master` feel free to change to a tag name from [runc version](https://github.com/opencontainers/runc/releases).
* `runc_make_buildtags`: Default to building with the `seccomp` and `selinux` build tags. Set to blank to not use any build tags.

Dependencies
------------

{ No other galaxy roles required }

Example Playbook
----------------

You can include this role in your playbook by referencing it as such:

    - hosts: servers
      roles:
         - { role: dougbtv.runc-ansible }

Testing
-------

To test this role, you may clone this git repo, and modify the `./inventory` file to suit your needs, and then run the playbook with:

```
ansible-playbook -i inventory test.yml
```

License
-------

MIT

Author Information
------------------

[@dougbtv](https://github.com/dougbtv) both twitter & github.
