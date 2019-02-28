[![Build Status](https://travis-ci.com/SpokeyWheeler/csdk.svg?branch=master)](https://travis-ci.com/SpokeyWheeler/csdk)
[![CodeFactor](https://www.codefactor.io/repository/github/spokeywheeler/csdk/badge)](https://www.codefactor.io/repository/github/spokeywheeler/csdk)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/1b5122e1b9fe43ce9c1882b3e332b0c3)](https://app.codacy.com/app/Zinaida/csdk)
[![DepShield Badge](https://depshield.sonatype.org/badges/SpokeyWheeler/csdk/depshield.svg)](https://depshield.github.io)

Role Name
=========

csdk

Requirements
------------

You need Informix install media and licenses

Role Variables
--------------

Defaults:

*   csdk_base_path: Starting point for all product installs - you can install multiple versions
*   csdk_install_path: Target path for install
*   csdk_tmp_path: Working directory - will be removed
*   csdk_version_previously_installed: false

Vars:

*   vendor: hcl or ibm
*   csdk_version: version number in full, e.g. 4.10.FC12W1
*   force_csdk_install: false or true
*   source_location_of_csdk_media: Either a path like "</tmp/installs>" or a URL like "<https://artifactory.example.com/media/hcl/informix/csdk/4.10.FC12W1>"

Dependencies
------------

None

Example Playbook
----------------

I expect an inventory group for csdk in the inventory file. This isn't really needed for this, but it will be needed when I eventually get around to integrating this into an all-encompassing cluster build.

```yaml
- hosts: csdk
  become: true

  roles:
    - { role: csdk }
```

License
-------

MIT

Author Information
------------------

<https://github.com/SpokeyWheeler>
