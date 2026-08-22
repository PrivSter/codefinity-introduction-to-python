# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this repository is

This is a personal collection of exercise solutions from Codefinity's
**"Introduction to Python"** course. It is a learning repo, not an
application or library — there is no package to install, no CLI to run, no
tests, and no build system. Each folder is a standalone answer to one course
exercise.

Because of this, treat every task here as "help write/fix a small, self
contained beginner Python script," not as "make a change across a codebase."
Don't introduce project scaffolding (requirements.txt, setup.py, test
suites, linters, CI, etc.) unless the user explicitly asks for it — that
would be over-engineering for what this repo is.

## Repository structure

Exercises are grouped by course module (top-level folder), and each
exercise gets its own subfolder containing a single `main.py`:

```
<course-module>/<exercise-name>/main.py
```

Current modules:
- `getting_started/` — first exercises (arithmetic, print statements)
  - `challenge_multiply_divide/main.py`
- `variables_and_types/` — variables, data types, naming
  - `variable_assignment/main.py`
  - `variable_calculations/main.py`
  - `variable_naming/main.py`

When adding a new exercise, follow this same pattern: create a new
`<module>/<exercise-name>/` folder (reusing an existing module folder if the
exercise belongs to that topic) with a `main.py` inside it.

## Conventions observed in existing solutions

- Plain Python 3, no external dependencies, no imports beyond the standard
  library (none of the current exercises need any).
- Output is produced with `print(...)`, often with a label string followed
  by the value(s): `print("Price per unit: $", item_price)`.
- Variable names are descriptive `snake_case` (`item_name`, `item_price`,
  `purchase_quantity`), matching the exercise's subject matter.
- A `# Testing` comment commonly precedes the block of `print` calls that
  exercises the variables/logic defined above it.
- Files are short (single digit to ~10 lines) and self-contained — keep new
  solutions in that same minimal style rather than adding classes, functions,
  or error handling that the exercise doesn't call for.

## Running the code

Each exercise is run directly with the standard interpreter, from within
its own folder or by path:

```bash
python3 <module>/<exercise-name>/main.py
```

There is nothing to install first.

## Working with this repo

- There is no test suite; verifying a change means running the script and
  checking the printed output matches what the exercise expects.
- Keep commits/exercises scoped to one folder at a time, mirroring the
  existing commit history (one exercise per commit, e.g. "Variable Naming",
  "Variable calculations").
- Do not add a `.git`-ignored virtualenv, dependency manifest, or tooling
  config unless asked — this repo intentionally has none.
