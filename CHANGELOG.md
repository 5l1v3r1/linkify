# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).
This project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html),
with the exception that 0.x versions can break between minor versions.

## [0.4.0] - 2019-08-05
### Changed
- Stop URLs when encountering ". This is consistent with RFC 3986, and
  it seems unlikely that a user would have an unescaped " in an URL
  anyway, as browsers escape it when copying an URL with it.
- Stop URLs at \` characters too, same as < and >
- Bump MSRV (minimal supported Rust version) to 1.31 (2018 edition)

## [0.3.1] - 2018-02-04
### Changed
- Bump memchr dependency to 2 (for wasm support)

## [0.3.0] - 2018-01-25
### Added
- New API to iterate over both plain text and link spans using the
  `spans` method. This is useful for iterating over all parts of the
  input, not just the detected links. Thanks @srijs!

## [0.2.0] - 2017-09-18
### Changed
- Don't autolink if authority is only "end" characters, e.g. like
  `http://.` or `http://"`

## [0.1.2] - 2017-06-09
### Fixed
- Fix `html_root_url` attribute

## [0.1.1] - 2017-06-08
### Added
- More docs
- Add `Debug` impls for `Links` and `LinkFinder`

## [0.1.0] - 2017-05-13
### Added
Initial release of linkify, a Rust library to find links such as URLs and email
addresses in plain text, handling surrounding punctuation correctly.


[0.4.0]: https://github.com/robinst/linkify/compare/0.3.1...0.4.0
[0.3.1]: https://github.com/robinst/linkify/compare/0.3.0...0.3.1
[0.3.0]: https://github.com/robinst/linkify/compare/0.2.0...0.3.0
[0.2.0]: https://github.com/robinst/linkify/compare/0.1.2...0.2.0
[0.1.2]: https://github.com/robinst/linkify/compare/0.1.1...0.1.2
[0.1.1]: https://github.com/robinst/linkify/compare/0.1.0...0.1.1
[0.1.0]: https://github.com/robinst/linkify/commits/0.1.0
