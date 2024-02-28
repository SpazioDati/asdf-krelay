# asdf-krealy

[krelay](https://github.com/knight42/krelay) plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```
asdf plugin-add krelay https://github.com/spaziodati/asdf-krelay.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of krelay.

## Architecture Override

The `ASDF_KRELAY_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `krelay` build to download. The primary use case is when attempting to install an older version of `krelay` for use on an Apple M1 computer as `krelay` was not built for ARM at the time.

### Without `ASDF_KRELAY_OVERWRITE_ARCH`:

```
% asdf install krelay 0.0.6
Downloading krelay from https://github.com/knight42/krelay/releases/download/v0.0.6/kubectl-relay_v0.0.6_linux-arm64.tar.gz
```

### With `ASDF_KRELAY_OVERWRITE_ARCH`:

```
% ASDF_KRELAY_OVERWRITE_ARCH=amd64 asdf install krelay 0.0.6
Downloading krelay from https://github.com/knight42/krelay/releases/download/v0.0.6/kubectl-relay_v0.0.6_linux-amd64.tar.gz
```
