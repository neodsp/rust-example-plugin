# My Plugin

1. cargo new --lib my_plugin
2. add this to Cargo.toml

```toml
[lib]
crate-type = ["cdylib"]

[dependencies]
nih_plug = { git = "https://github.com/robbert-vdh/nih-plug", features = [
    "assert_process_allocs",
] }
parking_lot = "0.12"
```

3. copy the defualt gain plugin to lib.rs https://github.com/robbert-vdh/nih-plug/blob/master/plugins/examples/gain/src/lib.rs

4. install build-tool

```bash
cargo install --git https://github.com/robbert-vdh/nih-plug.git cargo-nih-plug
```

5. build project

```bash
cargo nih-plug bundle my_plugin --release
```
