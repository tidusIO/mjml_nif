# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

For clarity, major releases of mjml_nif use the respective [mrml] releases with the same major release number.
I.e. `mjml_nif 0.x` versions use mrml versions `>= 0.1, < 1.0.0`, and `mjml_nif 1.x` versions use mrml versions `>= 1.0.0, < 2.0.0`, etc.

## [Unreleased]

---

## [1.3.2] - 2022-03-26
### Fixed
- Use [mrml] v1.2.10, which fixes a bug with parsing other self-closing tags
(see [mrml diff v1.2.9..v1.2.10][mrml-v1.2.9-v1.2.10]))

## [1.3.1] - 2022-03-25
### Fixed
- Use [mrml] v1.2.9, which fixes a bug with parsing the self-closing `br` and `meta` tags
(see [mrml diff v1.2.8..v1.2.9][mrml-v1.2.8-v1.2.9]))

## [1.3.0] - 2022-03-18
### Changed
- Use [Rustler Precompiled](https://github.com/philss/rustler_precompiled): this allows to use the mjml NIF without the Rust compiler 🎉
- Use [mrml] v1.2.8 (see [mrml diff v1.2.7..v1.2.8][mrml-v1.2.7-v1.2.8]))

## [1.2.0] - 2022-02-25
### Changed
- Update rustler to v0.24 (drops support for OTP <22, requires Elixir ~> 1.11)

## [1.1.3] - 2022-02-16
### Changed
- Update rustler to v0.23 (drops support for OTP 20)
- Use [mrml] v1.2.7, which allows inner elements in mj-social-element & mj-navbar-link (see [mrml diff v1.2.5..v1.2.7][mrml-v1.2.5-v1.2.7])

## [1.1.2] - 2021-10-04
### Changed
- Use [mrml] v1.2.5, which allows the `lang` attribute in the mjml tag and allows using `mj-raw` tags in `mj-head` (see [mrml diff v1.2.3..v1.2.5][mrml-v1.2.3-v1.2.5])

### Fixed
- Misc doc changes ([#31](https://github.com/adoptoposs/mjml_nif/pull/31))

## [1.1.1] - 2021-06-01
### Fixed
- Use [mrml] v1.2.3, which fixes a bug with ignored mj-class attributes (see [jdrouet/mrml #164](https://github.com/jdrouet/mrml/issues/164), [mrml diff v1.2.2..v1.2.3][mrml-v1.2.2-v1.2.3]))

## [1.1.0] - 2021-05-23
### Changed
- Use [mrml] v1.2.2
- Support OTP 24
- mjml_nif crate type changed from "dylib" to "cdylib"

## [1.0.0] - 2021-04-07
### Changed
- Use [mrml] v1.0.0
- Pass on parsing/rendering error messages from mrml to the error tuple of `MJML.to_html/1`

## [0.3.1] - 2021-02-23
### Fixed
- Compilation on aarch64 MacOS

## [0.3.0] - 2021-02-02
### Changed
- Use [mrml] v0.5.0

### Fixed
- Warning about special link args for x86_64-apple-darwin target

## [0.2.0] – 2020-10-19
### Changed
- Use [mrml] v0.3.3

## [0.1.0] – 2020-07-19
Initial release

[Unreleased]: https://github.com/adoptoposs/mjml_nif/compare/v1.3.2...HEAD
[1.3.2]: https://github.com/adoptoposs/mjml_nif/compare/v1.3.1...v1.3.2
[1.3.1]: https://github.com/adoptoposs/mjml_nif/compare/v1.3.0...v1.3.1
[1.3.0]: https://github.com/adoptoposs/mjml_nif/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/adoptoposs/mjml_nif/compare/v1.1.3...v1.2.0
[1.1.3]: https://github.com/adoptoposs/mjml_nif/compare/v1.1.2...v1.1.3
[1.1.2]: https://github.com/adoptoposs/mjml_nif/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/adoptoposs/mjml_nif/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/adoptoposs/mjml_nif/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/adoptoposs/mjml_nif/compare/v0.3.1...v1.0.0
[0.3.1]: https://github.com/adoptoposs/mjml_nif/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/adoptoposs/mjml_nif/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/adoptoposs/mjml_nif/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/adoptoposs/mjml_nif/compare/e77d33e9bcb58e0e2e9e522322d97ebdcb212618...v0.1.0
[mrml]: https://github.com/jdrouet/mrml

[mrml-v1.2.9-v1.2.10]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.9...mrml-core-1.2.10
[mrml-v1.2.8-v1.2.9]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.8...mrml-core-1.2.9
[mrml-v1.2.7-v1.2.8]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.7...mrml-core-1.2.8
[mrml-v1.2.5-v1.2.7]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.5...mrml-core-1.2.7
[mrml-v1.2.3-v1.2.5]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.3...mrml-core-1.2.5
[mrml-v1.2.2-v1.2.3]: https://github.com/jdrouet/mrml/compare/mrml-core-1.2.2...mrml-core-1.2.3
