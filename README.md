# Daniel Rosenbluth — VaultGhost Protocol

AI interaction provenance, attribution, and deterministic verification.

Live at: [https://drosenbluth25.github.io](https://drosenbluth25.github.io)

## What VaultGhost Is

VaultGhost is a protocol for recording and verifying AI interaction
artifacts. It produces signed, hash-chained records of declared inputs,
outputs, and metadata so that a captured interaction can be replayed and
checked for integrity after the fact.

## Evidence Boundary

VaultGhost verifies records within a captured boundary. It can verify
hashes, signatures, schemas, timestamps, declared metadata, verification
results, and replayable artifacts. It does not claim visibility into
hidden model weights, provider-side logs, undisclosed system prompts, or
private infrastructure.

## Core Repositories

- [vaultghost-protocol](https://github.com/drosenbluth25/vaultghost-protocol) — canonical protocol specification.
- [vaultghost-core](https://github.com/drosenbluth25/vaultghost-core) — reference implementation of core record and signing primitives.
- [vaultghost-verify](https://github.com/drosenbluth25/vaultghost-verify) — deterministic verification pipeline.
- [vaultghost-chain-ledger](https://github.com/drosenbluth25/vaultghost-chain-ledger) — hash-chained ledger of signed artifacts.
- [drosenbluth25](https://github.com/drosenbluth25/drosenbluth25) — GitHub profile repository.

## Verification Model

Verification is deterministic and operates only on captured records. A
verifier checks SHA-256 hashes of declared artifacts, Ed25519 signatures
over canonicalized record bodies, schema conformance, declared
timestamps and ordering against the hash chain, and replay of artifacts
against committed expected outputs. A verification run produces a pass
or fail result for the captured record set; it does not infer anything
about systems or processes outside that record set.

## Patent / IP Notice

A U.S. provisional patent application covering aspects of the VaultGhost
method was filed on 2026-02-25. The provisional filing establishes a
priority date only; it does not constitute a granted patent. The
canonical specification is published under Apache-2.0 and includes a
`CITATION.cff` file for academic reference.

## Current Status

Active development on the public protocol, reference implementation,
verification pipeline, and chain ledger. The spec is versioned and
tagged in `vaultghost-protocol`. Reference and verification components
track the spec.

## GitHub / Contact

GitHub: [github.com/drosenbluth25](https://github.com/drosenbluth25). For
protocol-level questions, please open an issue on
[vaultghost-protocol](https://github.com/drosenbluth25/vaultghost-protocol).
For security reports, follow the process described in `SECURITY.md` in
the relevant repository.
