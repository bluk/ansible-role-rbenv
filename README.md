ansible-role-rbenv
==================

[![GitHub license](https://img.shields.io/github/license/bluk/ansible-role-rbenv.svg)](https://github.com/bluk/ansible-role-rbenv/blob/master/LICENSE) [![Build Status](https://travis-ci.org/bluk/ansible-role-rbenv.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-rbenv)

An [Ansible](https://www.ansible.com) role to install [rbenv](https://github.com/rbenv/rbenv).

Requirements
------------

1. Add `rbenv` to your `$PATH` after install.

```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
```

2. Run the following:

```
~/.rbenv/bin/rbenv init
```

Role Variables
--------------

* `rbenv_install_path` - The path to install `rbenv`.

* `rbenv_git_url` - The git URL to clone `rbenv` from.

* `rbenv_git_update` - If the cloned `rbenv` git repository should be updated.

* `ruby_build_git_url` - The path to the `ruby-build` plugin for `rbenv`.

* `ruby_build_git_update` - If the cloned `ruby-build` git repository should be updated.

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.rbenv }
```

License
-------

Apache 2.0
