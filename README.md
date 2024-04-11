# docker-env

## Getting started

### Requirements

```
python3 -m pip install --user pipx
pipx install invoke
pipx install git-aggregator
pipx install pre-commit
pipx ensurepath
```

### Usage

Create folders

- src/local
- src/addons
- songs
- src/addons/custom

Create workspace file

```
invoke develop
```

Get Odoo and addons code with:

```
gitaggregate -c repos.yaml
```

Build image

```
invoke img-build --pull
```

Initialize a new empty database with:

```
invoke resetdb
```

Start Odoo with:

```
invoke start
```
