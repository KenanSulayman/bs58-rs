# bs58 [![travis-badge][]][travis] [![cargo-badge][]][cargo] [![license-badge][]][license] [![rust-version-badge][]][rust-version]

Another Rust [Base58][] codec implementation.

Compared to [`base58`][] this is significantly faster at decoding (about
2.4x as fast when decoding 32 bytes), almost the same speed for encoding
(about 3% slower when encoding 32 bytes), doesn't have the 128 byte
limitation and supports a configurable alphabet.

Compared to [`rust-base58`][] this is massively faster (over ten times as
fast when decoding 32 bytes, almost 40 times as fast when encoding 32
bytes), has no external dependencies and supports a configurable alphabet.

## Developing

This project uses [clippy][] and denies warnings in CI builds. To ensure your
changes will be accepted please check them with `cargo clippy` (available via
`cargo install clippy` on nightly rust) before submitting a pull request (along
with `cargo test` as usual).

Both the nightly date and clippy version used in CI are pinned in the
`.travis.yml` as clippy sometimes breaks for a few days after a new nightly is
published, feel free to update to a new known good pair anytime as part of a
pull request.

## License

Licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you shall be dual licensed as above, without any
additional terms or conditions.

[travis-badge]: https://img.shields.io/travis/mycorrhiza/bs58-rs/master.svg?style=flat-square
[travis]: https://travis-ci.org/mycorrhiza/bs58-rs
[cargo-badge]: https://img.shields.io/crates/v/bs58.svg?style=flat-square
[cargo]: https://crates.io/crates/bs58
[license-badge]: https://img.shields.io/badge/license-MIT/Apache--2.0-lightgray.svg?style=flat-square
[license]: #license
[rust-version-badge]: https://img.shields.io/badge/rust-1.13+-blue.svg?style=flat-square
[rust-version]: .travis.yml#L5

[Base58]: https://en.wikipedia.org/wiki/Base58
[`base58`]: https://github.com/debris/base58
[`rust-base58`]: https://github.com/nham/rust-base58
[clippy]: https://github.com/Manishearth/rust-clippy
