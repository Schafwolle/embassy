# embassy-sync

An [Embassy](https://embassy.dev) project.

Synchronization primitives and data structures with async support:

- [`Channel`](channel::Channel) - A Multiple Producer Multiple Consumer (MPMC) channel. Each message is only received by a single consumer.
- [`PriorityChannel`](channel::priority::PriorityChannel) - A Multiple Producer Multiple Consumer (MPMC) channel. Each message is only received by a single consumer. Higher priority items are sifted to the front of the channel.
- [`PubSubChannel`](pubsub::PubSubChannel) - A broadcast channel (publish-subscribe) channel. Each message is received by all consumers.
- [`Signal`](signal::Signal) - Signalling latest value to a single consumer.
- [`Mutex`](mutex::Mutex) - Mutex for synchronizing state between asynchronous tasks.
- [`Pipe`](pipe::Pipe) - Byte stream implementing `embedded_io` traits.
- [`WakerRegistration`](waitqueue::WakerRegistration) - Utility to register and wake a `Waker`.
- [`AtomicWaker`](waitqueue::AtomicWaker) - A variant of `WakerRegistration` accessible using a non-mut API.
- [`MultiWakerRegistration`](waitqueue::MultiWakerRegistration) - Utility registering and waking multiple `Waker`'s.

## Interoperability

Futures from this crate can run on any executor.

## Minimum supported Rust version (MSRV)

Embassy is guaranteed to compile on the latest stable Rust version at the time of release. It might compile with older versions but that may change in any new patch release.

## License

This work is licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  <http://www.apache.org/licenses/LICENSE-2.0>)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>)

at your option.
