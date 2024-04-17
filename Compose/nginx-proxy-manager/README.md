<p align="center">
    <img src="https://nginxproxymanager.com/logo.png" alt="Nginx Proxy Manager" width="75%">
</p>

## Introduction

Nginx Proxy Manager is een applicatie die je kan gebruiken om makkelijk een reverse proxy op te zetten.

## uitleg componenten

Maakt gebruik van SQLite als database en er is een healthcheck toegevoegd.

### SQLite

```yaml
environment:
  DB_SQLITE_FILE: "/data/database.sqlite"
```

### Healthcheck

```yaml
healthcheck:
  test: ["CMD", "/bin/check-health"]
  interval: 10s
  timeout: 3s
```

## Referenties

- [Nginx Proxy Manager][npm]
- [Docker Compose][compose]

[Dutchdomotics Discord](https://discord.gg/7ZVGJQwD)

<!-- LINKS -->
[npm]: https://nginxproxymanager.com
[compose]: https://docs.docker.com/compose/
```