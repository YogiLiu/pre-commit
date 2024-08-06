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
      - id: pytest
```
