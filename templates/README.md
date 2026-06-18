# templates/

Reference starter templates for new OpenTofu work. **Two ways to use them — pick what fits:**

| You want… | Use |
|---|---|
| A brand-new repo, pre-wired, with one click | The standalone **template repo**: [`thorvath-slower/tofu-template`](https://github.com/thorvath-slower/tofu-template) → "Use this template" (or `gh repo create <name> --template thorvath-slower/tofu-template`). Self-contained, has its own `validate` CI. |
| To copy a stack/layout into an existing repo, or just read the canonical shape | This mirror: **`templates/tofu-stack/`** (below). Copy the bits you need. |

> The standalone repo is the **canonical** source; `tofu-stack/` here is a kept-in-sync mirror for the copy-into-existing-repo case. Renovate keeps both current. If they ever diverge, the standalone repo wins.

## `tofu-stack/`
The canonical OpenTofu stack layout: `.opentofu-version` (version SSOT), `_shared/versions.tf` (provider SSOT, symlinked into stacks), an example `envs/dev/example/` stack wired to the `czid-tfstate-<account>-<region>` state foundation, a `validate` workflow, and `renovate.json`. See `tofu-stack/README.md` for the full walkthrough.

The canonical **conventions** (how we work, OpenTofu usage, upgrade runbooks) live once in **[`docs/platform/`](../docs/platform/README.md)** — the templates only carry the minimal seed files and point here.
