[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/rfay/ddev-copy-db/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/rfay/ddev-copy-db/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/rfay/ddev-copy-db)](https://github.com/rfay/ddev-copy-db/commits)
[![release](https://img.shields.io/github/v/release/rfay/ddev-copy-db)](https://github.com/rfay/ddev-copy-db/releases/latest)

# DDEV Copy Db

## Overview

This add-on integrates Copy Db into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get rfay/ddev-copy-db
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Copy Db |
| `ddev logs -s copy-db` | Check Copy Db logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.copy-db --copy-db-docker-image="ddev/ddev-utilities:latest"
ddev add-on get rfay/ddev-copy-db
ddev restart
```

Make sure to commit the `.ddev/.env.copy-db` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `COPY_DB_DOCKER_IMAGE` | `--copy-db-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@rfay](https://github.com/rfay)**
