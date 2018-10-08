Gitlab CI Runner
================
Install Gitlab CI Runner and register a runner.

Only docker executor is currently supported.

Only one runner can be registered per host each time the role is run. Already registered runners will be skipped if found by name or token. Runners removed from the GitLab CI server will be remove from the host.

This role adds the official repository, but leaves it disabled.

Requirements
------------
See `meta/main.yml`.

Role Variables
--------------
See `defaults/main.yml`.

Dependencies
------------
Docker needs to be installed, ie using some docker role in Ansible Galaxy.

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
- Activate `repo_gpgcheck`. Rpm from repository is not signed, but the repo itself is, however yum gets into validation problems of the repo.

Licence
-------
Released under the [MIT license](https://opensource.org/licenses/MIT).

Author Information
------------------
Luis Gracia while at [EMBL-EBI](http://www.ebi.ac.uk/):
- luis.gracia [at] ebi.ac.uk
- GitHub at [luisico](https://github.com/luisico)
- Galaxy at [luisico](https://galaxy.ansible.com/luisico)
