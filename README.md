stackage-cli
============

[![Build Status](https://travis-ci.org/fpco/stackage-cabal.svg)](https://travis-ci.org/fpco/stackage-cabal)

A command-line interface for leveraging stackage.

You must have `ghc`, `ghc-pkg`, and `cabal` on your $PATH. This program will make various calls to those executables on your behalf.

This package provides the following stackage plugins:

## stackage init

Downloads a `cabal.config` file from `stackage.org`. That's all it does! The `cabal.config` file constrains the package versions used to build your project. Stackage.org is constantly calculating the best compatible build plans for a big subset of Hackage.

## stackage purge

Calls `ghc-pkg unregister` on your package databases. (You will be prompted on a per-db basis; use `stackage purge --force` if you don't want to be prompted.) This is an easy way to clean out your sandbox.

## stackage upgrade

A `stackage purge` followed by `stackage init`.
