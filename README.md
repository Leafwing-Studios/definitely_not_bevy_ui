# About

A heavily experimental fork of [bevy_ui](https://github.com/bevyengine/bevy/tree/main/crates/bevy_ui), designed for tight ECS-first UI integration with the open source Rust game engine [Bevy](https://bevyengine.org/). 

You should expect, in the long-run, that this work is merged back upstream, if only in conceptual form.
When that happens, this library will be archived. 
Until then, feel free to use and contribute to this!

May it give you the ECS-powered UI you've always dreamt of.

## Instructions

### Getting started

Add this project to your crate's `Cargo.toml`.

For usage, check out the provided examples!

## Contributing

See [CONTRIBUTING.md](https://github.com/Leafwing-Studios/template-repo/blob/main/CONTRIBUTING.md)!

### Testing

1. Use doc tests aggressively to show how APIs should be used.
You can use `#` to hide a setup line from the doc tests.
2. Unit test belong near the code they are testing. Use `#[cfg(test)]` on the test module to ignore it during builds, and `#[test]` on the test functions to ensure they are run.
3. Integration tests should be stored in the top level `tests` folder, importing functions from `lib.rs`.

Use `cargo test` to run all tests.

### CI

The CI will:

1. Ensure the code is formatted with `cargo fmt`.
2. Ensure that the code compiles.
3. Ensure that (almost) all `clippy` lints pass.
4. Ensure all tests pass on Windows, MacOS and Ubuntu.

Check this locally with:

1. `cargo run -p ci`
2. `cargo test --workspace`

To manually rerun CI:

1. Navigate to the `Actions` tab.
2. Use the dropdown menu in the CI run of interest and select "View workflow file".
3. In the top-right corner, select "Rerun workflow".

### Documentation

Reference documentation is handled with standard Rust doc strings.
Use `cargo doc --open` to build and then open the docs.

Design docs (or other book-format documentation) is handled with [mdBook](https://rust-lang.github.io/mdBook/index.html).
Install it with `cargo install mdbook`, then use `mdbook serve --open` to launch the docs.
