# Changelog

All notable changes to the Hyperspace Lighting integration are documented in this file.

## 1.0.6

### Removed

- **WLED update entity** — its install path could never work on Hyperspace devices (it always failed with "Current version is unknown"), and it offered stock WLED releases, which are not valid firmware for Hyperspace devices. The entity is removed entirely; update HyperCubes through Hyperspace's own update channel.
- **WLED GitHub version checks** — the integration no longer queries the WLED releases API during refreshes.
