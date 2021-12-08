---
layout: default
title: Role Development Guidelines
rank: 3
---

# Role Development Guidelines

- Always install and use the latest version of ansible-lint. As of 02-Dec-2021, it's ansible-lint-5.3.0. Install with:
`# pip3 install ansible-lint --user`

- Put the following two files in the home directory of each role:
https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.ansible-lint
https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.yamllint.yml 

- Put the following file into directory .github/workflow of each role:
https://github.com/berndfinger/sap-preconfigure/blob/bz2003630/.github/workflows/ansible-lint.yml 
This will trigger an ansible-lint run on GitHub after each git push.

