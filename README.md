[![Build Status](https://github.com/MarcoGorelli/abs-imports/workflows/tox/badge.svg)](https://github.com/MarcoGorelli/abs-imports/actions?workflow=tox)
[![Coverage](https://codecov.io/gh/MarcoGorelli/abs-imports/branch/main/graph/badge.svg)](https://codecov.io/gh/MarcoGorelli/abs-imports)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/MarcoGorelli/abs-imports/main.svg)](https://results.pre-commit.ci/latest/github/MarcoGorelli/abs-imports/main)

abs-imports
===========

A pre-commit hook to automatically convert relative imports to absolute.

## Installation

```
pip install abs-imports
```

## Usage as a pre-commit hook

See [pre-commit](https://github.com/pre-commit/pre-commit) for instructions

Sample `.pre-commit-config.yaml`:

```yaml
-   repo: https://github.com/MarcoGorelli/abs-imports
    rev: v0.1.2
    hooks:
    -   id: abs-imports
```

## Command-line example

```console
$ cat mypackage/myfile.py
from . import __version__
$ abs_imports mypackage/myfile.py
$ cat mypackage/myfile.py
from mypackage import __version__
```

## See also

Check out [pyupgrade](https://github.com/asottile/pyupgrade), which I learned a lot from when writing this.
