Gitlab CI Runner
================
Install Gitlab's CI Multi runner and register a runner.

Only docker executor is currently supported.

This role adds the official repository, but leaves it disabled.

Requirements
------------
See `meta/main.yml`.

Role Variables
--------------
See `defaults/main.yml`.

Dependencies
------------
Docker needs to be installed.

Example Playbook
----------------
Example:
```
- hosts: servers
  roles:
    - docker
    - gitlab-ci-runner
```

TODO
----
- Better way of finding already registered runners.
- Allow runners to pick jobs without tags.
- Add link to docker role in readme.
- Activate `repo_gpgcheck`. Rpm from repository is not signed, but the repo itself is, however yum gets into validation problems of the repo.

Licence
-------
Licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

Author Information
------------------
Luis Gracia <luis.gracia@ebi.ac.uk>
