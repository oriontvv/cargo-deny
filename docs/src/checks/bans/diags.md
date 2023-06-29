# Bans diagnostics

### `banned`

A crate which is [explicitly banned](cfg.md#the-allow-and-deny-fields-optional) was detected.

### `allowed`

A crate which is [explicitly allowed](cfg.md#the-allow-and-deny-fields-optional) was detected.

### `not-allowed`

When using [`bans.allow`](cfg.md#the-allow-and-deny-fields-optional), a crate was detected that wasn't in that list.

### `duplicate`

One or more [duplicate versions](cfg.md#the-multiple-versions-field-optional) of the same crate were detected.

### `skipped`

A crate version that matched an entry in [`bans.skip`](cfg.md#the-skip-field-optional) was encountered.

### `wildcard`

A crate was included via a [wildcard dependency](cfg.md#the-wildcards-field-optional) by one or more crates.

### `unmatched-skip`

A crate version in [`bans.skip`](cfg.md#the-skip-field-optional) was not encountered.

### `allowed-by-wrapper`

A crate in `bans.deny` was allowed since it was directly depended on by a [`wrappers`](cfg.md#the-wrappers-field-optional) crate.

### `unmatched-wrapper`

A crate in `bans.deny` had one or more [`wrappers`](cfg.md#the-wrappers-field-optional) crates, but a crate not in that list had a direct dependency on the banned crate.

### `skipped-by-root`

A crate was skipped from being checked as a duplicate due to being transitively referenced by a crate version in [`bans.skip-tree`](cfg.md#the-skip-tree-field-optional).

### `unmatched-root`

A crate version in [`bans.skip-tree`](cfg.md#the-skip-tree-field-optional) was not encountered.

### `build-script-not-allowed`

A crate which has been denied because it has a build script but is not part of the [`bans.allow-build-script`](cfg.md#the-allow-build-scripts-field-optional) list.

### `exact-features-mismatch`

A crate's features do not exactly match the configured feature set, and [`bans.features.exact`](cfg.md#the-features-exact-field-optional) is `true`.

### `feature-banned`

An enabled crate feature is present in the [`bans.features.deny`](cfg.md#the-features-deny-field-optional) list.

### `unknown-feature`

A feature in either [`bans.features.deny`](cfg.md#the-features-deny-field-optional) or [`bans.features.allow`](cfg.md#the-features-allow-field-optional) does not exist for the crate.

### `default-feature-enabled`

The `default` feature was enabled on a crate, and the [`bans.external-default-features`](cfg.md#the-external-default-features-field-optional) or [`bans.workspace-default-features`](cfg.md#the-workspace-default-features-field-optional) was configured.