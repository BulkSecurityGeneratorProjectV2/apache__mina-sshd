# [Version 2.1.0 to 2.2.0](./docs/changes/2.2.0.md)

# [Version 2.2.0 to 2.3.0](./docs/changes/2.3.0.md)

# [Version 2.3.0 to 2.4.0](./docs/changes/2.4.0.md)

# [Version 2.4.0 to 2.5.0](./docs/changes/2.5.0.md)

# [Version 2.5.0 to 2.5.1](./docs/changes/2.5.1.md)

# [Version 2.5.1 to 2.6.0](./docs/changes/2.6.0.md)

# [Version 2.6.0 to 2.7.0](./docs/changes/2.7.0.md)

# [Version 2.7.0 to 2.8.0](./docs/changes/2.8.0.md)

# [Version 2.8.0 to 2.9.0](./docs/changes/2.9.0.md)

# [Version 2.9.0 to 2.9.1](./docs/changes/2.9.1.md)

# Planned for next version

## Bug fixes

* [SSHD-1293](https://issues.apache.org/jira/browse/SSHD-1293) ExplicitPortForwardingTracker does not unbind auto-allocated port
* [SSHD-1294](https://issues.apache.org/jira/browse/SSHD-1294) Close MinaServiceFactory instances properly
* [SSHD-1297](https://issues.apache.org/jira/browse/SSHD-1297) Avoid OutOfMemoryError when reading a public key from a corrupted Buffer

## Major code re-factoring

## Potential compatibility issues

## Minor code helpers

* New utility method `KeyUtils.loadPublicKey()` to read a public key file.

## Behavioral changes and enhancements

* Netty I/O back-end: respect configurations for `CoreModuleProperties.SOCKET_BACKLOG` and `CoreModuleProperties.SOCKET_REUSEADDR`.
* MINA I/O back-end: use `CoreModuleProperties.NIO2_READ_BUFFER_SIZE` for the initial read buffer size, if set.
  A new `CoreModuleProperties.MIN_READ_BUFFER_SIZE` can be set to control the minimum read buffer size (64
  bytes by default in Apache MINA).
