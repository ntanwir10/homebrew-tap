# GuardScan channel catalog

This repository is the public shared Homebrew and Scoop catalog for
[`ntanwir10/GuardScan`](https://github.com/ntanwir10/GuardScan). It contains:

- `Formula/guardscan.rb` for Homebrew
- `bucket/guardscan.json` for Scoop
- `channel-lock.json`, which binds both generated files to one immutable
  GuardScan release manifest and source commit

GuardScan release automation owns catalog contents. Do not edit generated
formulae, manifests, or the lock by hand. Catalog pull requests must reproduce
byte-for-byte from the exact GuardScan commit named in `channel-lock.json`.

The catalog is a generated projection, not a source mirror or a second release
authority. Its verification workflow is sourced from GuardScan so catalog
policy changes are reviewed with the release generator.

Before the first verified stable native release, the catalog intentionally
contains only this README and its verification workflow. The workflow treats
that exact empty publication state as healthy; partial metadata is rejected.
The release train creates the formula, Scoop manifest, and cryptographic lock
together in one pull request.
