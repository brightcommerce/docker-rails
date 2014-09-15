# Docker Rails

Dockerfile to build a base container image for Rails projects. Installs and configures git, nodejs, rbenv, ruby-build, bundler and supporting libraries like curl, ssl, readline, yaml, xml and xslt.

## Table Of Contents

- [Version](#version)
- [How To Use](#how-to-use)
- [Configuration](#configuration)
    - [Ports](#ports)
    - [Specifying Ruby Versions](#specifying-ruby-versions)
- [Copyright](#copyright)

## Version

The current release (4.1.5.20140915) contains scripts to install dependencies for Ruby on Rails 4.1.5 using Ruby 2.1.2p95. You can howver specify alternative ruby versions in the `rubies.txt` file (one ruby version per line) and these versions will be installed and bundler will be setup for each version. Our version numbers will reflect the version of Rails being installed.

## How To Use

This repository is intended to be used as a base layer for Rails projects. To specify this as a base, just include the `FROM` key in the Dockerfile of your Rails project. For example:

``` bash
FROM brightcommerce/rails:4.1.5.20140915
```

## Configuration

### Ports

This installation exposes port `80`.

### Specifying Ruby Versions

Specifies each version of ruby to be installed by adding them to the `rubies.txt` file, one per line. Bundler will be installed for each version of ruby specified. By default this repository only specifies one version of ruby which is currently `2.1.2p95`.

## Copyright

Copyright 2014 Brightcommerce, Inc.
