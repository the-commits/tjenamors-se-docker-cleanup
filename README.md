[![sourcehut](https://img.shields.io/badge/sourcehut-~the--commits/tjenamors--se--docker--cleanup-2d6b9e?logo=sourcehut)](https://git.sr.ht/~the-commits/tjenamors-se-docker-cleanup)
[![GitHub mirror](https://img.shields.io/badge/GitHub-the--commits/tjenamors--se--docker--cleanup-181717?logo=github)](https://github.com/the-commits/tjenamors-se-docker-cleanup)

# docker_cleanup

An Ansible role to prune dangling Docker resources (images, containers, volumes, networks).

## Installation

Add to `requirements.yml`:

```yaml
roles:
  - name: docker_cleanup
    src: git@git.sr.ht:~the-commits/tjenamors-se-docker-cleanup
    scm: git
    version: main
```

## Variables

| Variable | Default | Description |
|---|---|---|
| `docker_cleanup_auto` | `false` | Run cleanup on every playbook run |
| `docker_cleanup_dangling_only` | `false` | Only prune dangling images (`true`) or all unused (`false`) |
| `docker_cleanup_prune_volumes` | `false` | Also prune unused volumes (use with caution) |

## Example

```yaml
- hosts: all
  become: true
  vars:
    docker_cleanup_auto: true
    docker_cleanup_prune_volumes: false
  roles:
    - role: docker_cleanup
```

## License

AGPL-3.0
