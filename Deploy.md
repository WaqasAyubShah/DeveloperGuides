Install Rust & Cargo 

1) Install

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

2. Run test validator

```bash
solana-test-validator
```

    3. Create project & get in the folder

```bash
cargo init hello_world --lib
cd hello_world
```

    4. Add the`solana-program`

```bash
cargo add solana-program
```

Tip:  Add this if above don't work

```
cargo add solana-program@"=1.17.17"
```

    5. Open your`Cargo.toml` file and add these

```toml
[lib]
name = "hello_world"
crate-type = ["cdylib", "lib"]
```

    6. Build you rust program now

```bash
cargo build-bpf
```

    7. Deploy it with

```bash
solana program deploy ./target/deploy/hello_world.so
```


#### Congratulations! [#](https://solana.com/developers/guides/getstarted/local-rust-hello-world#congratulations)

You have successfully setup, built, and deployed a Solana program using the Rust language.
