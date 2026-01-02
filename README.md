# Rust Book Labs

A small Rust playground repo for learning and experimenting whilst working through [*The Rust Programming Language*](https://doc.rust-lang.org/book/).

This repo is a **Cargo workspace** containing multiple crates:

- **`sandpit/`** — a grab-bag crate for small throwaway scripts.
  - Most 'toy' programs live as separate binaries in `sandpit/src/bin/` (one file = one executable).
- **Future crates** — anything more substantial (e.g. a bigger project, longer-running tutorial build, etc.) gets its own dedicated crate under the workspace root.

## Layout

```text
.
├── Cargo.toml            # workspace manifest
├── sandpit/
│   ├── Cargo.toml
│   └── src/
│       ├── main.rs
│       └── bin/
│           ├── fibonacci.rs
│           └── ...
└── <future-projecy>
    ├── Cargo.toml
    └── src/...
```

## How-to

* Build everything in the workspace
    * `cargo build`

* Test everything
    * `cargo test`

* Run a specific crate (package)
    * `cargo run -p sandpit`

* Run a specific binary inside sandpit/src/bin
    * `cargo run -p sandpit --bin fibonacci`