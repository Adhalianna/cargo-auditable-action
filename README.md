# Cargo-Auditable Build Action

Installs and runs `cargo-auditable` which replaces `cargo build` command and extends the binary with SBOM data. Read [more about cargo-auditable here](https://github.com/rust-secure-code/cargo-auditable).

## Usage

### Input parameters

All of the following are optional:

- `args`: The arguments that will be passed to the cargo build command which is a part of the process executed by cargo-auditable.
- `toolchain`: The Rust toolchain to use, e.g. _nightly_, defaults to _stable_
- `cargo_auditable_version`: The version of cargo-auditable that should be fetched from [crates.io](https://crates.io/). Defaults to the latest version.

## Implementation

This action is a composite that builds upon:
- [baptiste0928/cargo-install](https://github.com/baptiste0928/cargo-install)
- [actions/checkout](https://github.com/actions/checkout/)
- [actions-rs/cargo](https://github.com/actions-rs/cargo/)

Read the details at [baptiste0928/cargo-install](https://github.com/baptiste0928/cargo-install) to learn more about __security considerations__ of that action.