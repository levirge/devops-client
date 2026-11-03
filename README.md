# devops-client

The Levirge DevOps client: a small static Linux binary that runs behind your firewall and connects
outbound to Levirge DevOps over NATS, so you can monitor and manage databases, logs, Docker and
hosts without opening inbound ports.

This repository currently hosts release binaries. Source will follow.

## Releases

- **Latest release** (`stable`): <https://github.com/levirge/devops-client/releases/latest>
- **`canary`** prerelease: rebuilt from every change to the main branch.

Each release has `devops-client-linux-amd64`, `devops-client-linux-arm64`, a `.sha256` for each,
and `VERSION`.

```bash
curl -LO https://github.com/levirge/devops-client/releases/latest/download/devops-client-linux-amd64
curl -LO https://github.com/levirge/devops-client/releases/latest/download/devops-client-linux-amd64.sha256
sha256sum -c devops-client-linux-amd64.sha256
```
