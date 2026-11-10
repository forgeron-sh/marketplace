# marketplace

A Forgeron marketplace: finished tools, one per folder of `tools/`, published as GitHub Releases
and listed in `forgeron-marketplace.json`. Read [docs/lifecycle.md](docs/lifecycle.md) first.

## Commands

- `forgeron init <name>` at the root: a new tool in `tools/<name>/`, listed in the index.
- In `tools/<name>/`: `forgeron test`, `forgeron change ...`, then `forgeron release` on `main`
  and `git push --follow-tags`. The tag `<name>@<version>` runs `.github/workflows/release.yml`:
  it tests, bundles, attaches the bundle to the release and updates the index.

## Rules

- A workspace installs the latest release of each tool and updates it when a newer one is published:
  a release is what its users get.
- `README.md` is for admins and may be technical; `GUIDE.md` is for the people who use the tool,
  with no technical term.
- No real secret in the repository, its tests or its fixtures.
