osstrtools
======

osstrtools is a small library that adds some helper methods which are useful when working with raw OsStr. What Rust provides by itself is pretty lacking when you need to do some manipulation on those types.

This mostly usefuly when you're doing low-level stuff with files. I factored this library out of ![hunter](https://github.com/rabite0/hunter), so for the most part it contains stuff I needed there, plus a bit more I stopped using.

Available methods and their singatures are:

```rust
fn split(&self, pat: &OsStr) -> Vec<OsString>;
fn split_lines(&self) -> Vec<OsString>;
fn replace(&self, from: &OsStr, to: &OsStr) -> OsString;
fn trim_last_space(&self) -> OsString;
fn trim_end_newlines(&self) -> &OsStr;
fn contains_osstr(&self, pat: &OsStr) -> bool;
fn position(&self, pat: &OsStr) -> Option<usize>;
fn splice_quoted(&self, from: &OsStr, to: Vec<OsString>) -> Vec<OsString>;
fn splice_quoted_single(&self, from: &OsStr, to: Vec<OsString>) -> Vec<OsString>;
fn splice_with(&self, from: &OsStr, to: Vec<OsString>) -> Vec<OsString>;
fn quote(&self) -> OsString;
fn quote_single(&self) -> OsString;
fn escape_single_quote(&self) -> OsString;
```

If the demand is there I'm willing to add more, just ask and I'll see what I can do.
