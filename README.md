# 🏭 UDS Package Trust Manager

[![Latest Release](https://img.shields.io/github/v/release/defenseunicorns/uds-package-trust-manager)](https://github.com/defenseunicorns/uds-package-trust-manager/releases)
[![Build Status](https://img.shields.io/github/actions/workflow/status/defenseunicorns/uds-package-trust-manager/tag-and-release.yaml)](https://github.com/defenseunicorns/uds-package-trust-manager/actions/workflows/tag-and-release.yaml)
[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/defenseunicorns/uds-package-trust-manager/badge)](https://api.securityscorecards.dev/projects/github.com/defenseunicorns/uds-package-trust-manager)

This package is designed for use as part of a [UDS Software Factory](https://github.com/defenseunicorns/uds-software-factory) bundle deployed on [UDS Core](https://github.com/defenseunicorns/uds-core).

## Pre-requisites

The Trust Manager Package expects to be deployed on top of [UDS Core](https://github.com/defenseunicorns/uds-core) with the dependencies listed below being configured prior to deployment.

#### Cert Manager

Trust Manager depends on resources deployed as part of Cert Manager so that must be installed first. The [UDS Cert Manager Package](https://github.com/defenseunicorns/uds-package-cert-manager) can be used for this. See the example uds-bundle.yaml in this repo for an example.

## Flavors

| Flavor | Description | Example Creation |
| ------ | ----------- | ---------------- |
| `upstream` | Uses upstream images within the package. | `zarf package create . -f upstream` |

## Releases

The released packages can be found in [ghcr](https://github.com/defenseunicorns/uds-package-trust-manager/pkgs/container/packages%2Fuds%2Ftrust-manager).

## UDS Tasks (for local dev and CI)

*For local dev, this requires you install [uds-cli](https://github.com/defenseunicorns/uds-cli?tab=readme-ov-file#install)

> [!TIP]
> To get a list of tasks to run you can use `uds run --list`!

## Contributing

Please see the [CONTRIBUTING.md](./CONTRIBUTING.md)
