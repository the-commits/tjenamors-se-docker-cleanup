# AGENTS.md — tjenamors-se-docker-cleanup

## Critical: No Real Data in Git

Public role repo. No real IPs, hostnames, or secrets.

## Repo

- `git@git.sr.ht:~the-commits/tjenamors-se-docker-cleanup`
- Role name in `galaxy.yml`: `docker_cleanup`
- Repo naming: `tjenamors-se-<role>`
- Pushing to a new git.sr.ht URL auto-creates it

## Commits

- GPG-sign: `git commit -S`

## Development

```bash
molecule test   # requires vagrant-libvirt
```
