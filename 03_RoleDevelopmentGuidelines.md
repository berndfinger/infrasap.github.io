---
layout: default
title: Role Development Guidelines
rank: 3
---

# Role Development Guidelines

## Variable naming

Role variables need to be named as follows (example role name: sample_role)

- Role external variables start with the role name, as in:
```
sample_role_required_packages
```

- Role internal variables start with two underscores, followed by the role name, as in:
```
__sample_role_required_packages
```

- Role variables which store the result of a set_fact has the string "_fact" after the role name part, as in:
```
__sample_role_fact_required_packages
```

- Role variables which store the result of a function other than set_fact has the string "_register" after the role name part, as in:
```
__sample_role_register_installed_packages
```

## Ansible-lint cleaning

Ansible-lint cleaning is important so that a collection can be imported cleanly into Ansible Galaxy.

- Always install and use the latest version of ansible-lint. As of 02-Dec-2021, it's ansible-lint-5.3.0. Install with:
```
# pip3 install ansible-lint --user
```

- Put the following two files in the home directory of each role:
  - [.ansible-lint](https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.ansible-lint)
  - [.yamllint.yml](https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.yamllint.yml)

- Put the following file into directory .github/workflow of each role:
[.github/workflows/ansible-lint.yml](https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.github/workflows/ansible-lint.yml)
This will trigger an ansible-lint run on GitHub after each git push.

