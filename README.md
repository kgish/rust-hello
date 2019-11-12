# Hello

This is a simple hello application written in the [Rust programming language](https://www.rust-lang.org)

## Installation

First you will need to download and install Rust:

```
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Configure the PATH environment variable to include `~/.cargo/bin directory` in order to use the Rust toolchain, including `rustc`, `cargo`, and `rustup`. In the `.profile` file the following line will have been added:

```bash
export PATH="$HOME/.cargo/bin:$PATH"
```

Clone the repository like this:

```
$ git clone https://github.com/kgish/rust-hello.git
$ cd rust-hello
$ cargo run
```

## References

* [Rust programming language](https://www.rust-lang.org)
