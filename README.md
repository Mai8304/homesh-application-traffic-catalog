# Homesh Application Traffic Catalog

This repository publishes the signed application traffic identification catalog consumed by Homesh devices.

Device-facing resources are immutable or versioned under `/v1`:

- `v1/latest.json` activates one complete signed catalog generation.
- `v1/catalogs/{generation}.json` retains generation-addressable envelopes.
- `v1/objects/sha256/{digest}.json` stores atomic application records by content digest.

The catalog contains public identification rules only. It does not distribute App Store packages, device data, signing private keys, or router configuration. Authoring, review, signing, and verification remain in the private Homesh product repository; publication here must preserve those verified bytes exactly.

