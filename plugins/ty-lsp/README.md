# ty-lsp

Python language server (ty) for Claude Code, providing static type checking and code intelligence.

## Supported Extensions
`.py`, `.pyi`

## Installation

Install ty globally:

```bash
uv tool install ty@latest
```

Or with pip:

```bash
pip install ty
```

## Virtual Environment Detection

The plugin automatically detects and uses project virtual environments:

1. Walks up from the current working directory to find `pyproject.toml`
2. Activates `.venv/bin/activate` if found in that project root
3. Changes to the project root so ty discovers `pyproject.toml` configuration

### Monorepo Usage

For monorepos with multiple Python projects, start Claude Code from within the specific project directory:

```bash
# Instead of:
cd ~/Code/monorepo && claude

# Do this:
cd ~/Code/monorepo/my-python-project && claude
```

This ensures ty uses the correct project's `.venv` and `pyproject.toml`.

## More Information
- [ty on GitHub](https://github.com/astral-sh/ty)
- [ty Documentation](https://docs.astral.sh/ty/)
