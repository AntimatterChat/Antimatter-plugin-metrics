# Antimatter Metrics Plugin

The Antimatter Metrics Plugin is a versatile utility designed to collect and store various data points from the Antimatter application in [OpenMetrics](https://openmetrics.io/) format, similar to the functionality provided by [Prometheus](https://prometheus.io/). The primary purpose of this plugin is to facilitate troubleshooting by gathering metrics at regular intervals and allowing their inclusion in a dump file.

See the [Antimatter Product Documentation](https://antimatter.chat/docs/admins/apps.html#metrics) for details on installing, configuring, enabling, and using this Antimatter integration.

## How to Release

To trigger a release, follow these steps:

1. **For Patch Release:** Run the following command:
    ```
    make patch
    ```
   This will release a patch change.

2. **For Minor Release:** Run the following command:
    ```
    make minor
    ```
   This will release a minor change.

3. **For Major Release:** Run the following command:
    ```
    make major
    ```
   This will release a major change.

4. **For Patch Release Candidate (RC):** Run the following command:
    ```
    make patch-rc
    ```
   This will release a patch release candidate.

5. **For Minor Release Candidate (RC):** Run the following command:
    ```
    make minor-rc
    ```
   This will release a minor release candidate.

6. **For Major Release Candidate (RC):** Run the following command:
    ```
    make major-rc
    ```
   This will release a major release candidate.

## Feedback and support

Found a bug in the Metrics plugin, or missing a feature? Please [open an
issue](https://github.com/AntimatterChat/community/issues/new/choose) in the [Antimatter community
repository](https://github.com/AntimatterChat/community), where the feedback for every part of
Antimatter is gathered. Questions and ideas are welcome in its
[Discussions](https://github.com/AntimatterChat/community/discussions). Please report security
problems privately, as explained in the [security
policy](https://github.com/AntimatterChat/.github/blob/main/SECURITY.md).

## Development

### Operational Modes

In a High Availability (HA) environment, the Antimatter Metrics Plugin operates in two distinct modes: scraper mode and listener mode.

- **Scraper Mode:** In this mode, the plugin scrapes metrics from nodes listed in the `ClusterDiscovery` table. It also includes tsdb synchronization to a remote file store. This mode is essential for collecting metrics data.

- **Listener Mode:** In listener mode, the plugin serves download requests by copying tsdb blocks from the remote file store and preparing the dump. This mode is focused on making the collected metrics available for analysis and troubleshooting.

For the single node deployment, these two modes are combined.

### Contribution Guidelines

If you wish to contribute to the Antimatter Metrics Plugin, ensure you have the following versions installed:

- Go: version >= **1.20**
- NodeJS: version **16.x**
- NPM: version **7.x**

Feel free to join [AntimatterChat/community Discussions](https://github.com/AntimatterChat/community/discussions) to engage in discussions related to the project.

### License

See [LICENSE](LICENSE.txt) for licensing information. Your contributions to this open-source project are welcome!
