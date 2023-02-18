# tedge-container-sm-plugin

thin-edge.io software management plugin to install and start container on a device.

## Plugin description

The following thin-edge.io customization is included in the plugin.

* Monitor container status (up/down)
* Publish container metrics such as cpu, memory, network i/o

|Type|Yes/No|
|----|--|
|Software Management plugin|✅|
|Telemetry|✅|
|Service Health|✅|
|Operation handler|➖|


## Features

The plugin support the following docker compatible cli tools:

* docker
* podman
* nerdctl

## Packaging

The following linux package formats are provided on the releases page:

* deb (Debian/Raspbian)
* apk (Alpine Linux)
* rpm (RHEL/CentOS/Fedora)

## Building

To build the linux packages use the following steps:

1. Checkout the project

2. Install [nfpm](https://nfpm.goreleaser.com/install/)

3. Build the packages

    ```sh
    ./ci/build.sh
    ```

    Ideally the `SEMVER` environment variable should be set to the git tag, however
    you can also use a manual version using:

    ```sh
    ./ci/build.sh 1.0.1
    ```
