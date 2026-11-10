# Design decisions

Each entry records the choice, the alternatives, and why this one won.

## Package name: `matchbook`

- **Alternatives:** `pricetime`, `crossbook`, `fillwell`.
- **Why:** it matches the repo name, so there is only one name to remember.

## Layout: `src/matchbook/`

- **Alternative:** a `matchbook/` folder at the repo root.
- **Why:** Python can't import the code by accident from the current folder. Tests run against the installed package, the same way a user would run it.

## Environment: `uv`

- **Alternative:** `venv` plus `pip`.
- **Why:** `uv.lock` pins exact versions, so CI and my machine run the same dependencies.

## Dependencies: add them when needed

- **Alternative:** install the full tool list up front.
- **Why:** each dependency arrives with the milestone that uses it, so nothing sits unused and each one can be justified.
