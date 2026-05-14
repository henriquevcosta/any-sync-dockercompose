# Homelab overlay (this fork)

- **`homelab-networks.yml`** — attaches **`anytype-cli`** to external Docker network **`ai_internal`** so LiteLLM on the same VM can call `http://anytype-cli:31012` (see [ansible-nas](https://github.com/henriquevcosta/ansible-nas) `docs/anytype-homelab.md`).
- **`docker-compose.yml`** — **`anytype-cli`** / **`anytype-cli_bootstrap`** are enabled (upstream has them commented). Merge upstream changes periodically; resolve conflicts if upstream edits the same block.

Komodo runs this repo with **`docker-compose.yml`** + **`homelab-networks.yml`** (see `komodo/stacks/any_sync-aoi.toml` in ansible-nas after `make komodo-render`).
