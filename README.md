# sdc-amon-agent

**This is an experimental repository and is not yet production-ready**

*For now, the actual amon agent code used by Triton/Manta components is available at https://github.com/joyent/sdc-amon/*

This repository is part of the Joyent Triton project. See the [contribution
guidelines](https://github.com/joyent/triton/blob/master/CONTRIBUTING.md)
and general documentation at the main
[Triton project](https://github.com/joyent/triton) page.

The Triton Amon agent. This Triton component is deployed to all server
global zones and to most Triton and Manta service zone instances. It is
responsible for fetching probe configs from its amon-relay (ultimately
from the amon-master), running the configure probes, and sending events
for probe checks up to the master for alarming.


## Usage

For now, use the source.


## Development

The following sections are about developing this module.

### Building

TODO: engbld essentials

### Commiting

Before commit, ensure that the following passes:

    make check

### Releasing

Changes with possible user impact should:

1. Add a note to the [changelog](./CHANGES.md).
2. Bump the package version appropriately (major for breaking changes, minor
   for new features, patch for bug fixes).
3. Once merged to master, the new version should be tagged (currently this
   does not publish to npm) via:

        make cutarelease
