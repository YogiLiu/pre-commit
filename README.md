# pre-commit

My pre-commit hooks.

![GitHub Tag](https://img.shields.io/github/v/tag/YogiLiu/pre-commit)

## Install hooks

```bash
pre-commit install
```

## Usage

Create a `.pre-commit-config.yaml` file in the project root and add the following content:

```yaml
repos:
  - repo: https://github.com/YogiLiu/pre-commit
    rev: 0.2.0
    hooks:
      # Frontend
      - id: prettier
      - id: eslint
      - id: vitest

      # Python
      - id: ruff-lint
      - id: ruff-fmt
      - id: mypy

      # Go
      - id: gofmt
      - id: go-test
      - id: go-vet
      - id: goimports
```

## Extra

Since `pytest` cannot be define in third repo, there is a example for `pytest`:

```yaml
repos:
  - repo: local
    hooks:
      - id: pytest
        name: Pytest
        description: Test Framework for Python.
        entry: .venv/bin/pytest
        language: system
        types:
          - text
        files: ^.+\.py$|pyproject\.toml$
        pass_filenames: false
        minimum_pre_commit_version: 3.0.0
```

You can paste it to `.pre-commit-config.yaml`.
