# Forgeron marketplace

The official marketplace of [Forgeron](https://github.com/forgeron-sh/monorepo): finished tools a workspace installs, then updates when a newer release is published. A gateway reads it through `OFFICIAL_MARKETPLACE=forgeron-sh/marketplace`.

- Each tool lives in `tools/<name>/` and is listed in `forgeron-marketplace.json`.
- A release (`forgeron release` in the tool's folder, then `git push --follow-tags`) runs `.github/workflows/release.yml`: it tests the tool, bundles it, attaches the bundle to the release and updates the index.
- How a tool lives: [`docs/lifecycle.md`](docs/lifecycle.md). For agents: [`AGENTS.md`](AGENTS.md).

No tool is published here yet.
