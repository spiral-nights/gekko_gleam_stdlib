# AGENTS.md

## Project Overview

MoonBit-enabled fork of `gleam_stdlib` for use with `gekko`.

## Key Conventions & Invariants

- **Package name**: Keep `name = "gleam_stdlib"` unchanged in `gleam.toml`. Do not rename it.
- **MoonBit FFI**: MoonBit externals use `/// @external(moonbit, ...)` pragmas in `src/` backed by the MoonBit FFI package under `moonbit/` (`gleam_stdlib_ffi`).

## Verification

```sh
gleam test
./scripts/test_moonbit.sh
```

## Git

- Use conventional commit messages (e.g. `docs: add AGENTS.md`, `feat: ...`, `fix: ...`).
- Do not push unless explicitly asked.
