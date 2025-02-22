# deployKF - Command Line Interface (CLI)

[![Check Commit](https://github.com/deployKF/cli/actions/workflows/check-commit.yml/badge.svg)](https://github.com/deployKF/cli/actions/workflows/check-commit.yml)

This repo contains the command line interface (CLI) for [deployKF](https://github.com/deployKF/deployKF).

## Install

To install the `deploykf` CLI, please follow the [installation instructions](https://www.deploykf.org/guides/install-deploykf-cli/) on the deployKF website.

## Usage

The simplest usage of the `deploykf` CLI is to run the following command:

```bash
deploykf \
  --source-version 0.1.0 \
  --values ./custom-values.yaml \
  --output-dir ./GENERATOR_OUTPUT
```

This command will generate deployKF manifests in the `./GENERATOR_OUTPUT` directory using the `v0.1.0` source version and the values specified in your `./custom-values.yaml` file. 
Note that the `--source-version` flag must correspond to a tag from a [deployKF release](https://github.com/deployKF/deployKF/releases).

## Development

Here are some helpful commands when developing the CLI:

- `make build`: Builds the binary for your local platform and outputs it to `./bin/deploykf`.
- `make install`: Installs the binary to `/usr/local/bin`.
- `make lint`: Runs `golangci-lint` against the codebase to check for errors.
- `make lint-fix`: Attempts to automatically fix any linting errors found.
