Stouts.python
=============

[![Build Status](http://img.shields.io/travis/Stouts/Stouts.python.svg?style=flat-square)](https://travis-ci.org/Stouts/Stouts.python)
[![Galaxy](http://img.shields.io/badge/galaxy-Stouts.python-blue.svg?style=flat-square)](https://galaxy.python.com/list#/roles/910)
[![Tag](http://img.shields.io/github/tag/Stouts/Stouts.python.svg?style=flat-square)]()

Ansible role which manage python (pip, virtualenv)

#### Variables

```yaml
python_enabled: yes                 # The role is enabled
python_ppa: ppa:fkrull/deadsnakes   # Python PPA
python_version: 2.7                 # Set version (2.6, 2.7, 3.3, 3.4)
python_pip_executable: pip{{python_version}}
python_pip_latest:                  # Update python packages
- setuptools
- virtualenv
```

#### Usage

Add `Stouts.python` to your roles and set vars in your playbook file.

Example:

```yaml

- hosts: all

  roles:
    - Stouts.python

  vars:
    python_version: 3.4
```

#### License

Licensed under the MIT License. See the LICENSE file for details.

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Stouts/Stouts.python/issues)!
