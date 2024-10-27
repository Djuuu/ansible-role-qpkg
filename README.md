Ansible Role: QPKG
==================

Install or update QPKG packages on QNAP NAS.

- https://www.qnap.com/

Requirements
------------

A QNAP NAS.

Role Variables
--------------

Available role variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# QNAP Store apps
qpkg_apps: []
#  - container-station
#  - qufirewall
#  - MalwareRemover
#  - Qcenter
#  - Qcenter-Agent


# Third party apps
qpkg_3rd_party_apps: []
#  - repository_name: MyQnap
#    repository_url:  https://www.myqnap.org/repo.xml
#    apps:
#      - Entware
#      - Fdupes


# Unwanted apps to uninstall
qpkg_unwanted_apps: []
#  - helpdesk


# Wait for each operation
qpkg_wait_queue: true
# Number of retries when waiting for queue
qpkg_wait_retries: 30
# Seconds between each queue check
qpkg_wait_delay: 10
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: all
  gather_facts: false

  roles:
    - djuuu.qpkg
```

License
-------

Beerware License
