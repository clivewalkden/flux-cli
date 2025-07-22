# Flux

![GitHub Release](https://img.shields.io/github/v/release/clivewalkden/flux-cli)

Flux: a Magento patch config cleaner

## Features

- Cleans up Magento patch configurations

## Installation

Install the homebrew tap from my [homebrew-taps](https://github.com/clivewalkden/homebrew-taps) repo.

Then run:
`brew install clivewalkden/taps/flux`

## Usage

```
flux
```

Additional logging can be enabled by passing the `-v`, `-vv` or `-vvv` flags for verbose, debug, and trace logging respectively.

## Configuration

The configuration file should be placed in the git repository root directory and named `flux.yaml`. The file should look like this:

```yaml
ignore_list:
  - ACSD-xxxxx
magento_env_path: magento/.magento.env.yaml
ece_patches_bin: bin/ece-patches
```

The `ignore_list` is a list of patch names that should be ignored by the tool. The tool will add these patches to the `magento/.magento.env.yaml` file.

The `magento_env_path` is the path to the Magento environment configuration file where the patches will be added.

The `ece_patches_bin` is the path to the `ece-patches` binary that will be used to apply the patches.
