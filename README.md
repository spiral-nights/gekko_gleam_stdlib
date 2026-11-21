# stdlib

> **MoonBit / `gekko` Fork:** This is a modified fork of [`gleam-lang/stdlib`](https://github.com/gleam-lang/stdlib) for [`gekko`](https://github.com/spiral-nights/gekko) (see [`NOTICE`](./NOTICE) and [`LICENCE`](./LICENCE)). It preserves full Erlang and JavaScript compatibility while adding `/// @external(moonbit, ...)` pragmas and native MoonBit FFI backing packages under `moonbit/gleam_stdlib_ffi/`.
>
> Use it in a `gekko` target project's `gleam.toml`:
>
> ```toml
> [dependencies]
> gleam_stdlib = { git = "https://github.com/spiral-nights/gleam_stdlib.git", ref = "main" }
> ```
>
> Because the package name stays `gleam_stdlib`, transitive Hex dependencies requiring `gleam_stdlib` resolve automatically against this fork (provided `version` satisfies their SemVer constraint).

[![Package Version](https://img.shields.io/hexpm/v/gleam_stdlib)](https://hex.pm/packages/gleam_stdlib)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/gleam_stdlib/)
[![Discord chat](https://img.shields.io/discord/768594524158427167?color=blue)](https://discord.gg/Fm8Pwmy)

Gleam's standard library!
Documentation available on [HexDocs](https://hexdocs.pm/gleam_stdlib/).

## Installation

Add `gleam_stdlib` to your Gleam project.

```sh
gleam add gleam_stdlib@1
```
```gleam
import gleam/io

pub fn greet(name: String) -> Nil {
  io.println("Hello " <> name <> "!")
}
```

## Targets

Gleam's standard library supports Erlang and JavaScript, and this fork adds **MoonBit** (`wasm-gc`, `wasm`, `js`, and `native`) via [`gekko`](https://github.com/spiral-nights/gekko).

### Compatibility

This library is compatible with all versions of Erlang/OTP 26 and higher, 
as well as all NodeJS, Deno, Bun, and major browsers that are currently
supported by their maintainers. If you have a compatibility issue with
any platform open an issue and we'll see what we can do to help.
