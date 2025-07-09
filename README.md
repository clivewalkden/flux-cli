# Flux

Flux: a Magento patch config cleaner

## Features

- Cleans up Magento patch configurations

## Usage

```
flux
```

## Configuration

The configuration file should be placed in the git repository root directory and named `flux.yaml`. The file should look like this:

```yaml
ignore_list:
  - ACSD-xxxxx
magento_env_path: magento/.magento.env.yaml
```

The `ignore_list` is a list of patch names that should be ignored by the tool. The tool will add these patches to the `magento/.magento.env.yaml` file.

The `magento_env_path` is the location of the `.magento.env.yaml` in relation to the root of your project.

