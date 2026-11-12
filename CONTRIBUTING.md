# Contributing

Code contributions are by invitation only. Read [docs/contributing.md](docs/contributing.md) for the full policy and review process.

## Local setup

1. Install Rust via [rustup](https://rustup.rs). The pinned toolchain in `codex-rs/rust-toolchain.toml` is picked up automatically.
2. Install the helper tools: `cargo install --locked just cargo-nextest cargo-insta`.
3. For repo-wide formatting of Markdown/JSON, install Node 22+ and pnpm 10.33+, then run `pnpm install`.
4. Clone and build:

   ```bash
   git clone https://github.com/testcapyai/codex.git
   cd codex/codex-rs
   cargo build
   cargo run --bin codex -- "explain this codebase to me"
   ```

## Before opening a PR

- `just fmt` to format Rust code.
- `just fix -p <crate>` to apply Clippy fixes for the crate you touched.
- `cargo test -p <crate>` for the changed crate (`just test` runs the full suite).
- `pnpm format` if you edited Markdown, JSON, or workflow files.

See [docs/install.md](docs/install.md) for more build details and [AGENTS.md](AGENTS.md) for code conventions.
