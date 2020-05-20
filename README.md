GitHub Keys
=========

Install authorized_keys into a given user. Fetches the public keys from GitHub 
for specified users, or users in specified organizations.

Requirements
------------

None

Role Variables
--------------

* `github_keys_install_user` : username to install keys into
* `github_keys_create_install_user` : set false to assume the system user
    already exists
    * Default: `true`
* `github_keys_github_orgs` : array of github organization to get public keys
    from
    * Default: `[]`
* `github_keys_github_users` : array of additional github users to get public
    keys from
    * Default: `[]`
* `github_keys_additional_keys` : array of additional public keys to add to
    authorized_keys
    * Default: `[]`
* `github_keys_force_refresh` : True to force a fetch of keys, even if they
    appear to be loaded already
    * Default: `false`
* `github_keys_stale_auth_days` : Time for when the authorized_key file
    hasn't been modified that it is force updated regardless of
    the `github_keys_force_refresh` setting. A setting of `false` will not trigger,
    expected to be a number when not false
    * Default: `false`

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: smartlogic.github_keys, github_keys_install_user: "deploy" }

License
-------

MIT

Author Information
------------------

SmartLogic. http://SmartLogic.io
