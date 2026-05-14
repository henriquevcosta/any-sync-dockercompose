# Homelab overlay (this fork)

- **`homelab-networks.yml`** — keeps **`anytype-cli`** on the stack **default** network (so it still reaches **`netcheck`** and peers) and adds **`ai_internal`** with alias **`anytype-cli`** so LiteLLM can use `http://anytype-cli:31012`.
- **`docker-compose.yml`** — **`anytype-cli`** / **`anytype-cli_bootstrap`** are enabled (upstream has them commented). Merge upstream changes periodically; resolve conflicts if upstream edits the same block.

Komodo runs this repo with **`docker-compose.yml`** + **`homelab-networks.yml`** (see `komodo/stacks/any_sync-aoi.toml` in ansible-nas after `make komodo-render`).
