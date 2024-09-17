# rustls-platform-verifier-lto-bug

This repository was adapted from [here](https://github.com/Thomas-Avery/test-rustls-platform-verifier). The goal of this repository is to provide an example project showcasing a potential bug in the [rustls-platform-verifier crate](https://github.com/rustls/rustls-platform-verifier), to aid in identifying and fixing a potential bug.

GitHub Issue Link: {will be added once filed}

## The Issue

There is a potential linking issue when compiling this project on Windows for the `x86_64-pc-windows-gnu` target.

## Reproduce

1. Install Rust
2. Clone the repository on a x86_64 Windows machine. This bug was reproduced on a machine with the following information:
    - OS: `Windows 10 Pro`
    - Version: `22H2`
    - OS Build: `19045.4894`
    - System type: `64-bit operating system, x64-based processor`
3. Run: `cargo build --target x86_64-pc-windows-gnu --release > .\log.txt 2>&1`
4. You will see the error in `log.txt`
