# Changes

## 2.0.0

Added checks if the removal of users doesn't appear to work correctly
due to a problem reading the folder that it didn't also create, causing an assertion failure and
suggesting a force refresh with `github_keys_force_refresh: true`

### Breaking Changes

* Due to the assert message handling, this now requires Ansible 2.8

## 1.0.0

Instead of time based refresh, the role now compares the installed keys on the file system with the current member lists
and cleans up without intervention. See the Breaking Changes below.

### Breaking Changes

* Time based param `github_keys_stale_auth_days` is no longer used

* Due to the standardization of set comparison and lowercasing of usernames, a forced refresh is required
  the first time verion 1.0.0 is used
