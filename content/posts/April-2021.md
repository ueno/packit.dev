---
title: "April 2021"
date: 2021-04-09T16:40:16+01:00
weight: 76
---

## Week 14 (April 4th - April 9th)

- Honza converted packit's test suite from STI to FMF and configured packit to
  synchronize the suite to Fedora dist-git
  ([packit#1192](https://github.com/packit/packit/pull/1192)).
- Franta fixed a bug in packit which kept only appending targets to an existing
  COPR project which is no longer a case - dropped targets are now being
  removed
  ([packit#1197](https://github.com/packit/packit/pull/1197)).

## Week 15 (April 12th - April 16th)

- Tomáš fixed an issue in chaining variable definitions in the RPM macros used
  to set up source-git repositories with `packit init`
  ([packit#1206](https://github.com/packit/packit/pull/1206)).
- Jirka improved the error message Packit Service emits when the request to
  start a test in Testing Farm fails
  ([packit-service#1055](https://github.com/packit/packit-service/pull/1055)).
- Laura made Packit Service to set a status for jobs as soon as the requests
  are received, and before starting any of the jobs
  ([packit-service#1046](https://github.com/packit/packit-service/pull/1046)).
  This way users will receive a more immediate feedback about the Service
  handling their requests.

## Week 16 (April 19th - April 23th)

- The `current_version_command` and `create_tarball_command` config options are being deprecated
  in favour of [actions](https://packit.dev/docs/actions/).
  An issue will be created in the affected repositories if we find those options in use.
  ([packit-service#1064](https://github.com/packit/packit-service/pull/1064))
- The result pages have been replaced by the views on our dashboard.
  Let us know what do you think about that and what information do you want to see there.
  You can expect more changes on this field.
  - The result views have been implemented by [@IceWreck](https://github.com/IceWreck)
    ([dashboard#73](https://github.com/packit/dashboard/pull/73)).
  - The integration on packit-service side has been done by [Maťo](https://github.com/mfocko)
    ([packit-service#1056](https://github.com/packit/packit-service/pull/1056),
    [dashboard#95](https://github.com/packit/dashboard/pull/95)).

## Week 17 (April 26th - April 30th)

- When initiating a new source-git repo, packit adds info about sources to packit.yaml.
  Also dist-git sources from the lookaside cache are not commited.
  ([packit#1208](https://github.com/packit/packit/pull/1208),
  [packit#1216](https://github.com/packit/packit/pull/1216)).
- Franta added support for git repository cache into packit. The service part is yet to be done
  ([packit#1214](https://github.com/packit/packit/pull/1214)).
- Service reacts to `/packit` commands only when they appear alone on a line
  ([packit-service#1065](https://github.com/packit/packit-service/pull/1065),
  [packit-service#1083](https://github.com/packit/packit-service/pull/1083)).
- Service doesn't create duplicate issues when configuration is invalid
  ([packit-service#1075](https://github.com/packit/packit-service/pull/1075)).
- We deprecated `current_version_command` and `create_tarball_command` in packit config
  ([packit#1212](https://github.com/packit/packit/pull/1212)).
