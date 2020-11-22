<div align="center">
 <img src="https://github.com/mitsuhiko/insta/blob/master/assets/logo.png?raw=true" width="250" height="250">
 <p><strong>insta: a snapshot testing library for Rust</strong></p>
</div>

## Introduction

Snapshots tests (also sometimes called approval tests) are tests that
assert values against a reference value (the snapshot). This is similar
to how `assert_eq!` lets you compare a value against a reference value but
unlike simple string assertions, snapshot tests let you test against complex
values and come with comprehensive tools to review changes.

Snapshot tests are particularly useful if your reference values are very
large or change often.

## What it looks like:

```rust
#test
fn test_hello_world() {
    insta::assert_debug_snapshot!(vec!1, 2, 3);
}
```

Curious? There is a screencast that shows the entire workflow: [watch the insta
introduction screencast](https://www.youtube.com/watch?v=rCHrMqE4JOY&feature=youtu.be).
Or if you're not into videos, read the [one minute introduction](#introduction).

Insta also supports inline snapshots which are stored right in your source file
instead of separate files. This is accomplished by the companion
[cargo-insta](https://crates.io/crates/cargo-insta) tool.

## License and Links

- [Issue Tracker](https://github.com/mitsuhiko/insta/issues)
- [Documentation](https://docs.rs/insta/)
- License: Apache-2.0
