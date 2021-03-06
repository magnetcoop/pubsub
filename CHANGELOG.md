# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [0.3.5] - 2020-09-23
### Added
- Added `ig/suspend-key!` and `ig/resume-key` Integrant keys so that we don't disconnect and reconnect when executing `(reset)` in Duct dev environments unless the configuration for the keys have changed.

## [0.3.4] - 2020-08-08
### Fixed
- The fix in 0.3.3 for custom SSL configurations was only applied to the MQTT implementation. The fix is now applied to the AMQP implementation too.
- The underlying libraries can throw exceptions in the publish, subscribe, unsubscribe, etc. operations. We now catch them and return sensible values in each case.

## [0.3.3] - 2020-07-08
### Fixed
- Only apply custom SSL configuration when defined. Before it was always applied when we specified that the connection used SSL, even if it was not defined. Now we only apply it when it is explicitly defined.

## [0.3.2] - 2020-05-02
### Changed
- Bumped dependencies to newer versions

### Added
- Added this changelog

## [0.3.1] - 2019-02-26
### Changed
- Bumped minimum Leiningen version to 2.9.0
- Reorganized dev profile definition
- Fixed typos in README.md and added more examples

### Added
- Add Travis CI integration
- Add deployment configuration and integration tests CI 

## [0.3.0] - 2019-02-26
- Initial commit (previous versions were not publicly released)

[UNRELEASED]: https://github.com/magnetcoop/pubsub/compare/v0.3.5...HEAD
[0.3.5]: https://github.com/magnetcoop/pubsub/compare/v0.3.4...v0.3.5
[0.3.4]: https://github.com/magnetcoop/pubsub/compare/v0.3.3...v0.3.4
[0.3.3]: https://github.com/magnetcoop/pubsub/compare/v0.3.2...v0.3.3
[0.3.2]: https://github.com/magnetcoop/pubsub/compare/v0.3.1...v0.3.2
[0.3.1]: https://github.com/magnetcoop/pubsub/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/magnetcoop/pubsub/releases/tag/v0.3.0
