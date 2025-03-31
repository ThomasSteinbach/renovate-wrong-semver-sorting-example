# 35108

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

## Current behavior

When using `separateMultipleMinor=true` and thus having multiple minor version upgrade PRs, I noticed that Renovate sorts SemVer versions alphabetically instead of numerical.

Wrong sorting example: `1.1.0` -> `1.10.0` -> `1.2.0`

See the order of PRs in the dependency dashboard.
This is also the order of PRs processed, when `automerge=true`.

👉 https://github.com/ThomasSteinbach/renovate-wrong-semver-sorting-example/issues/12

## Expected behavior

Expected sorting: `1.1.0` -> `1.2.0` -> `...` -> `1.10.0`

## Link to the Renovate issue or Discussion

👉 https://github.com/renovatebot/renovate/discussions/35108