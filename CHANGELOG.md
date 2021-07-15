# Changes

## 1.0.0

Instead of time based refresh, the role now compares the installed keys on the file system with the current member lists
and cleans up without intervention. See the Breaking Changes below.

### Breaking Changes

* Time based param `github_keys_stale_auth_days` is no longer used

* While nothing should break, this update will clean out old folders that are not in use,
  the download of specific GitHub username keys now standardizes on all lowercase naming.
  If you used username based keys, it is suggested that you do a force refresh, unless every username
  ever used was already completely lowercased.
