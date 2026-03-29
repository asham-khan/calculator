# CLAUDE.md — Project Guidelines for Claude Code

This file provides coding standards, architecture notes, and instructions for Claude when working on this repository.

## Project Overview

This is a Python calculator application. The main entry point is `app.py`.

## Language & Runtime

- **Language**: Python 3.10+
- **No external dependencies** unless explicitly added to a `requirements.txt`

## Code Style

- Follow PEP 8 for all Python code
- Use 4 spaces for indentation (no tabs)
- Maximum line length: 88 characters (Black-compatible)
- Use descriptive variable and function names (e.g., `calculate_result` not `calc`)
- Add type hints to all function signatures
- Write docstrings for all public functions and classes

## Naming Conventions

- Functions/variables: `snake_case`
- Classes: `PascalCase`
- Constants: `UPPER_SNAKE_CASE`
- Private methods: prefix with underscore (e.g., `_validate_input`)

## Testing

- Write unit tests for all new functions using `unittest` or `pytest`
- Test files should be named `test_*.py` or `*_test.py`
- Aim for >80% code coverage on new code
- Run tests before submitting a PR: `python -m pytest`

## Error Handling

- Always handle edge cases: division by zero, invalid input, overflow
- Raise specific exceptions with descriptive messages
- Never silently swallow exceptions — log or re-raise them

## Git & PR Practices

- Keep PRs small and focused on a single concern
- Write clear commit messages in imperative mood (e.g., "Add division function")
- Reference related issues in PR descriptions

## Claude-Specific Instructions

- When asked to fix a bug, explain the root cause before proposing a fix
- When adding a feature, also add corresponding tests
- When refactoring, do not change observable behavior
- Always check for edge cases in arithmetic operations (zero division, negative numbers, floats)
- Prefer readable code over clever one-liners
