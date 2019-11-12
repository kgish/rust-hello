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


## Repository

Clone the repository like this:

```
$ git clone https://github.com/kgish/rust-hello.git
$ cd rust-hello
$ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/hello`
Hello, world!
```


## New dependency

Following the getting started guide, update the `cargo.toml` file to include a new dependency:

```
[dependencies]
ferris-says = "0.1"
```

and modify the `main.rs` file to look like this:

```
use ferris_says::say;
  use std::io::{stdout, BufWriter};
  
  fn main() {
      let stdout = stdout();
      let out = b"Hello fellow Rustaceans!";
      let width = 24;
  
      let mut writer = BufWriter::new(stdout.lock());
      say(out, width, &mut writer).unwrap();
  }
```

Now when you run the application, you should see the following:

```
$ cargo run
   Compiling hello v0.1.0 (/home/kiffin/projects/rust/hello)
    Finished dev [unoptimized + debuginfo] target(s) in 0.33s
     Running `target/debug/hello`
----------------------------
| Hello fellow Rustaceans! |
----------------------------
              \
               \
                  _~^~^~_
              \) /  o o  \ (/
                '_   -   _'
                / '-----' \

```


## References

* [Rust programming language](https://www.rust-lang.org)
