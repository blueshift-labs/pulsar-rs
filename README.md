## pulsar-rs: Future-based Rust client for [Apache Pulsar](https://pulsar.apache.org/)

[![crates](https://img.shields.io/crates/v/pulsar.svg)](https://crates.io/crates/pulsar)
[![docs](https://img.shields.io/docsrs/pulsar)](https://docs.rs/pulsar)

[Documentation](https://docs.rs/pulsar)

This is a pure Rust client for Apache Pulsar that does not depend on the C++ Pulsar library. It provides an async/await based API, compatible with [Tokio](https://tokio.rs/) and [async-std](https://async.rs/).

Features:

- URL based (`pulsar://` and `pulsar+ssl://`) connections with DNS lookup
- multi topic consumers (based on a regex or list)
- TLS connection
- configurable executor (Tokio or async-std)
- automatic reconnection with exponential back off
- message batching
- compression with LZ4, zlib, zstd or Snappy (can be deactivated with Cargo features)
- telemetry using [tracing](https://github.com/tokio-rs/tracing) crate (can be activated with Cargo features)

### Getting Started

Add the following dependencies in your `Cargo.toml`:

```toml
futures = "0.3"
pulsar = "5.1"
tokio = "1.0"
```

Try out [examples](examples):

- [producer](examples/producer.rs)
- [consumer](examples/consumer.rs)
- [reader](examples/reader.rs)

### License

This library is licensed under the terms of both the MIT license and the Apache License (Version 2.0), and may include packages written by third parties which carry their own copyright notices and license terms.

See [LICENSE-APACHE](LICENSE-APACHE), [LICENSE-MIT](LICENSE-MIT), and [COPYRIGHT](COPYRIGHT) for details.
