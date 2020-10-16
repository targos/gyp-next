# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## 0.1.0 (2020-10-16)


### Features

* hoist shared libs to PRODUCT_DIR for all platforms ([1248a9d](https://www.github.com/targos/gyp-next/commit/1248a9dea3b49f47c236153bff76d89d6e7874f7))
* port "add support for MSVC cross-compilation" from node ([72ea11b](https://www.github.com/targos/gyp-next/commit/72ea11b74407fcb2ffb41ec7d330008b2b5f6d81))
* support source files with duplicate basename ([#62](https://www.github.com/targos/gyp-next/issues/62)) ([72eddfe](https://www.github.com/targos/gyp-next/commit/72eddfe67f0216c3109f59efdb38dd9a2f8dddc5))


### Bug Fixes

* do not rewrite absolute paths to avoid long paths ([#74](https://www.github.com/targos/gyp-next/issues/74)) ([c2ccc1a](https://www.github.com/targos/gyp-next/commit/c2ccc1a81f7f94433a94f4d01a2e820db4c4331a))
* **msvs:** correctly rename object files for absolute paths ([#71](https://www.github.com/targos/gyp-next/issues/71)) ([f2c7618](https://www.github.com/targos/gyp-next/commit/f2c761838babf11024a3e6fab96d1e5a9dc1f556))
* compile_commands.json generation ([#22](https://www.github.com/targos/gyp-next/issues/22)) ([afa06c4](https://www.github.com/targos/gyp-next/commit/afa06c4d2d612ef9cff86eedad53e7503d1453fb))
* port ab4aca868d from upstream ([#11](https://www.github.com/targos/gyp-next/issues/11)) ([6f4834e](https://www.github.com/targos/gyp-next/commit/6f4834e9c38c91d5369b8c1e585e8fc8e58decb0))
* upstream 50317c3 from nodejs/node ([1db1392](https://www.github.com/targos/gyp-next/commit/1db139210c8c60a1e32f636b6962c534f49dc502)), closes [/github.com/nodejs/node/commit/50317c38a4511914e5eb69d6f05f290087887cf7#diff-50366fa1de3b4a645c172ab704f9155](https://www.github.com/targos//github.com/nodejs/node/commit/50317c38a4511914e5eb69d6f05f290087887cf7/issues/diff-50366fa1de3b4a645c172ab704f9155)

## [Unreleased]

## [0.6.1] - 2020-10-14

### Fixed
- Correctly rename object files for absolute paths in MSVS generator.

## [0.6.0] - 2020-10-13

### Added
- The Makefile generator will now output shared libraries directly to the product
  directory on all platforms (previously only macOS).

## [0.5.0] - 2020-09-30

### Added
- Extended compile_commands_json generator to consider more file extensions than
  just `c` and `cc`. `cpp` and `cxx` are now supported.
- Source files with duplicate basenames are now supported.

### Removed
- The `--no-duplicate-basename-check` option was removed.
- The `msvs_enable_marmasm` configuration option was removed in favor of
  auto-inclusion of the "marmasm" sections for Windows on ARM.

## [0.4.0] - 2020-07-14

### Added
- Added support for passing arbitrary architectures to Xcode builds, enables `arm64` builds.

### Fixed
- Fixed a bug on Solaris where copying archives failed.

## [0.3.0] - 2020-06-06

### Added
- Added support for MSVC cross-compilation. This allows compilation on x64 for
  a Windows ARM target.

### Fixed
- Fixed XCode CLT version detection on macOS Catalina.

## [0.2.1] - 2020-05-05

### Fixed
- Relicensed to Node.js contributors.
- Fixed Windows bug introduced in v0.2.0.

## [0.2.0] - 2020-04-06

This is the first release of this project, based on https://chromium.googlesource.com/external/gyp
with changes made over the years in Node.js and node-gyp.

[Unreleased]: https://github.com/nodejs/gyp-next/compare/v0.6.1...HEAD
[0.6.1]: https://github.com/nodejs/gyp-next/compare/v0.6.0...v0.6.1
[0.6.0]: https://github.com/nodejs/gyp-next/compare/v0.5.0...v0.6.0
[0.5.0]: https://github.com/nodejs/gyp-next/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/nodejs/gyp-next/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/nodejs/gyp-next/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/nodejs/gyp-next/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/nodejs/gyp-next/releases/tag/v0.2.0
