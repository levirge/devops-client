<p align="left">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/levirge-devops-logo-dark.svg">
    <img src="assets/levirge-devops-logo-light.svg" alt="Levirge DevOps" width="420">
  </picture>
</p>

[![version](https://img.shields.io/github/v/release/levirge/devops-client?label=version&color=d99a3a)](https://github.com/levirge/devops-client/releases/latest)

# Levirge DevOps client — runs inside your firewall

**One small binary next to your systems. Outbound only, no ports to open.**

The client is the part of [Levirge DevOps](https://github.com/levirge/devops) that runs on your
hosts. It connects out to the platform over NATS, so your team and your AI agents can query
SQL, Redis, MongoDB and InfluxDB, inspect Docker and NATS, read logs and watch host and
llama.cpp metrics on machines you can't reach from the internet.

- One static Linux binary for amd64 or arm64, with no runtime or libraries to install.
- Read-only unless a connection and the caller's role both allow writes.
- Connection credentials stay on the host; only names and status go over the bus.

This repository hosts release binaries. Source will follow.

## Download

```bash
curl -LO https://github.com/levirge/devops-client/releases/latest/download/devops-client-linux-amd64
curl -LO https://github.com/levirge/devops-client/releases/latest/download/devops-client-linux-amd64.sha256
sha256sum -c devops-client-linux-amd64.sha256
```

Use `devops-client-linux-arm64` on ARM hosts. Then create a provisioning token in the app and run
`devops-client --token=<token>`.

## Releases

- **Latest release** (`stable`): <https://github.com/levirge/devops-client/releases/latest>
- **`canary`** prerelease: rebuilt from every change to the main branch.

Each release has `devops-client-linux-amd64`, `devops-client-linux-arm64`, a `.sha256` for each,
and `VERSION`.

## Links

- **App / sign in:** <https://devops.levirge.com>
- **Agent plugin (Claude Code, Codex):** <https://github.com/levirge/devops>
- **Levirge:** <https://levirge.com/devops>
