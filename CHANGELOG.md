## v0.2.0 [2021-02-18]
_What's new?_
* Add support for multiregion queries. ([#197](https://github.com/turbot/steampipe/issues/197))
* Add support for connection config. ([#173](https://github.com/turbot/steampipe/issues/173))
* Add `plugin update` command. ([#176](https://github.com/turbot/steampipe/issues/176))
* Add automatic checking of plugin versions. ([#164](https://github.com/turbot/steampipe/issues/164))
* Add caching of query results. This is disabled by default but may be enabled by setting `STEAMPIPE_CACHE=true`
  NOTE: It is expected this will be updated to default to true in the next patch release. ([#11](https://github.com/turbot/steampipe-postgres-fdw/issues/11)) 
* Log whether Steampipe is running in Windows subsystem for Linux. ([#171](https://github.com/turbot/steampipe/issues/171))
* All env vars should have STEAMPIPE_ prefix. ([#172](https://github.com/turbot/steampipe/issues/172))
* Display null column values as <null> instead of an empty string. ([#186](https://github.com/turbot/steampipe/issues/186))
* Validate that plugins do not have an sdk version greater than the version steampipe is built against. ([#183](https://github.com/turbot/steampipe/issues/183))

_Bug fixes_
* Fix hitting a space after a meta-command causing runtime error. ([#182](https://github.com/turbot/steampipe/issues/182))

## v0.1.3 [2021-02-11]

_What's new?_
* Add 'line' output format. ([#114](https://github.com/turbot/steampipe/issues/114))
* Log files older than 7 days are deleted. ([#121](https://github.com/turbot/steampipe/issues/121))

_Bug fixes_
* Fix multi line editing issues. ([#103](https://github.com/turbot/steampipe/issues/103))
* Fix command-Right breaking for unicode chars ([#9](https://github.com/turbot/steampipe/issues/9))
* Fix 'no unpinned buffers available' error.  ([#122](https://github.com/turbot/steampipe/issues/122))
* Fix database installation failure for certain Linux configurations. ([#133](https://github.com/turbot/steampipe/issues/133))

## v0.1.2 [2021-02-04]

_What's new?_
* The `.inspect` command no longer requires the fully qualified name for tables. ([#21](https://github.com/turbot/steampipe/issues/21))
* The helper function `glob` has been added. ([#134](https://github.com/turbot/steampipe/issues/134))
* The output of the `plugin install` command now shows the installed version.  ([#93](https://github.com/turbot/steampipe/issues/93))
* The `.help` command now displays a link to the inline help docs.  ([#92](https://github.com/turbot/steampipe/issues/92))
* The wait spinner is now only shown in interactive mode. ([#106](https://github.com/turbot/steampipe/issues/106))

_Bug fixes_
* Fix JSON and bool columns displaying as strings. ([#95](https://github.com/turbot/steampipe/issues/95))
* Fix column headings displaying in upper case.  ([#94](https://github.com/turbot/steampipe/issues/94))

## v0.1.1 [2021-01-28]

_What's new?_
* A new meta-command `.help` has been added.  ([#54](https://github.com/turbot/steampipe/issues/54))
* After `steampipe plugin install`, a link to the plugin docs is displayed.
* A spinner is now displayed for slow queries. ([#77](https://github.com/turbot/steampipe/issues/77))
* A maximum column width of 1024 is now enforced - content longer than this will wrap. ([#12](https://github.com/turbot/steampipe/issues/12))
* The `description` column of the `.inspect` command now fills the available horizontal screen space. ([#11](https://github.com/turbot/steampipe/issues/11))
* The Linux installation package now uses tar instead of zip. ([#63](https://github.com/turbot/steampipe/issues/63))

_Bug fixes_
* Fix results paging failure for very long rows (> 64k chars). ([#75](https://github.com/turbot/steampipe/issues/75))
* Fix invalid query resulting in the database session remaining open. ([#60](https://github.com/turbot/steampipe/issues/60))
* Fix data formatting in json output. ([#14](https://github.com/turbot/steampipe/issues/14))
* Fix incorrect plugin hub link.
* Fix `steampipe query` panic when exiting after `service stopped --force` has been run. ([#38](https://github.com/turbot/steampipe/issues/38))
* Fix `runtime error: slice bounds out of range [1:0]`.  ([#40](https://github.com/turbot/steampipe/issues/40))
* Fix boolean meta-command showing wrong status when no parameter is passed. ([#48](https://github.com/turbot/steampipe/issues/48))