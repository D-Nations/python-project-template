# python-project-template

## Setup

### 0. Install uv

Install `uv` from the official installer.

Windows:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

macOS/Linux:

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Restart your terminal, then verify the install:

```sh
uv --version
```

### 1. Sync dependencies

From the repository root:

```sh
uv sync --dev --upgrade
```

This creates the local virtual environment and installs the project development tools.

### 2. Install Git hooks

```sh
uv run prek install
```

After this, `prek` will run the configured checks automatically before commits.

## VS Code

Install these VS Code extensions for the best editor experience:

- Ruff
- ty

## Command Aliases

Adding `just-rust` to the development dependencies and creating a `justfile` is a great way to add project command
aliases.

For example, a `justfile` can provide short commands for common workflows such as formatting, linting, testing, and
running all checks.
