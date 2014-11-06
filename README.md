Stouts.python
=============

[![Build Status](http://img.shields.io/travis/Stouts/Stouts.python.svg?style=flat-square)](https://travis-ci.org/Stouts/Stouts.python)
[![Galaxy](http://img.shields.io/badge/galaxy-Stouts.python-blue.svg?style=flat-square)](https://galaxy.ansible.com/list#/roles/910)

Ansible role which manage python's versions (pip, virtualenv)

#### Variables

```yaml
python_enabled: yes                 # The role is enabled
python_ppa: ppa:fkrull/deadsnakes   # Python PPA
python_versions: [2.7, 3.4]         # Set versions (2.6, 2.7, 3.3, 3.4) which will be installed

python_install: []                  # Set packages to install
```

#### Usage

Add `Stouts.python` to your roles and set vars in your playbook file.

Example:

```yaml

- hosts: all

  roles:
    - Stouts.python

  vars:
    python_versions: [2.7, 3.3]
    python_install: [django, gunicorn]
```

#### License

Licensed under the MIT License. See the LICENSE file for details.

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Stouts/Stouts.python/issues)!
