[![Build Status](https://travis-ci.org/georust/proj-sys.svg?branch=master)](https://travis-ci.org/georust/proj-sys)

# Low-level bindings for PROJ v7.1.x

**This is a
[`*-sys`](https://doc.rust-lang.org/cargo/reference/build-scripts.html#a-sys-packages)
crate; you shouldn't use its API directly.** See the
[`proj`](https://github.com/georust/proj) crate for general use.

A guide to the functions can be found here:
https://proj.org/development/reference/functions.html. 

By default, the crate will search for an existing `libproj` (via `PROJ v7.1.x`)
installation on your system using
[pkg-config](https://www.freedesktop.org/wiki/Software/pkg-config/). 

If an acceptable installation is not found, proj-sys will attempt to build
libproj from source bundled in the crate.

## Features

`bundled_proj` - forces building libproj from source even if an acceptable
version could be found on your system.  Note that SQLite3 and `libtiff` must be
present on your system if you wish to use this feature, and that it builds
`libproj` **without** its native network functionality; you will have to
implement your own set of callbacks if you wish to make use of them (see the
[`proj`](https://crates.io/crates/proj) crate for an example).

## License

Licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
