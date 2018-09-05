# Changelog

All Notable changes to `sebastiaanluca/php-codesniffer-ruleset` will be documented in this file.

Updates should follow the [Keep a CHANGELOG](http://keepachangelog.com/) principles.

## Unreleased

## 0.1.3 (2018-09-05)

### Changed

- Don't require underscore prefix for private methods
- Don't worry about missing namespaces in migrations
- Ignore multi line array with single value
- Ignore multiline arrays that have a single value
- Ignore multiple function call arguments on a single line
- Ignore non-matching migration file/class names
- Ignore single line array with multiple values

### Fixed

- Ignore duplicate indent rule

## 0.1.2 (2018-09-05)

### Fixed

- Require depending packages as non-dev

## 0.1.1 (2018-09-05)

### Changed

- Added extra `composer.json` check scripts to the README

### Fixed

- Removed `basepath` from argument list

## 0.1.0 (2018-09-05)

### Added

- Added initial ruleset
