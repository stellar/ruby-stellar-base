# Changelog All notable changes to this project will be documented in this
file.  This project adheres to [Semantic Versioning](http://semver.org/).

As this project is pre 1.0, breaking changes may happen for minor version
bumps.  A breaking change will get clearly notified in this log.

## [Unreleased](https://github.com/stellar/ruby-stellar-base/compare/v0.3.0...HEAD)

### Changed
- BREAKING CHANGE: "Amounts", that is, input parameters that represent a
  certain amount of a given asset, such as the `:starting_balance` option for
  `Operation.create_account` are now interpreted using the convention of 7
  fixed-decimal places.  For example, specifying a payment where the amount is
  `50` will result in a transaction with an amount set to `500000000`.