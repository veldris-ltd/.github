<div align="center">

# Veldris

### Everything Open. Nothing Exposed.

Veldris builds **Midgard**, the sovereign AI and data operating environment for organisations where control of data, models, keys and infrastructure, and the ability to operate disconnected, are requirements rather than features.

[![Open source: Apache-2.0](https://img.shields.io/badge/open%20source-Apache--2.0-8C6526?labelColor=12161F)](https://github.com/veldris-ltd/midgard-app/blob/main/LICENSE)
[![Post-quantum by default](https://img.shields.io/badge/post--quantum-by%20default-8C6526?labelColor=12161F)](#design-principles)
[![ML-KEM: FIPS 203](https://img.shields.io/badge/ML--KEM-FIPS%20203-8C6526?labelColor=12161F)](https://csrc.nist.gov/pubs/fips/203/final)
[![ML-DSA: FIPS 204](https://img.shields.io/badge/ML--DSA-FIPS%20204-8C6526?labelColor=12161F)](https://csrc.nist.gov/pubs/fips/204/final)
[![SLH-DSA: FIPS 205](https://img.shields.io/badge/SLH--DSA-FIPS%20205-8C6526?labelColor=12161F)](https://csrc.nist.gov/pubs/fips/205/final)
<br>
[![Air-gap capable](https://img.shields.io/badge/air--gap-capable-8C6526?labelColor=12161F)](https://github.com/veldris-ltd/midgard-app#design-principles)
[![Built with Rust](https://img.shields.io/badge/built%20with-Rust-8C6526?labelColor=12161F&logo=rust&logoColor=white)](https://github.com/veldris-ltd/midgard-app)
[![Cyber Essentials certified](https://img.shields.io/badge/Cyber%20Essentials-certified-8C6526?labelColor=12161F)](https://veldris.io/security/)
[![Made in the UK](https://img.shields.io/badge/made%20in-the%20UK-8C6526?labelColor=12161F)](https://veldris.io/company/)

[Website](https://veldris.io) · [Midgard documentation](https://midgard.eu) · [Open source](https://veldris.io/open-source/) · [Security](https://veldris.io/security/) · [Contact](https://veldris.io/contact/)

</div>

---

## Midgard

<div align="center">

[![Licence](https://img.shields.io/github/license/veldris-ltd/midgard-app?label=licence&labelColor=12161F&color=CA1D25)](https://github.com/veldris-ltd/midgard-app/blob/main/LICENSE)
[![CI](https://github.com/veldris-ltd/midgard-app/actions/workflows/ci.yml/badge.svg)](https://github.com/veldris-ltd/midgard-app/actions/workflows/ci.yml)
[![Acceptance gate: 72 of 72, air-gapped](https://img.shields.io/badge/acceptance%20gate-72%2F72%20air--gapped-CA1D25?labelColor=12161F)](https://github.com/veldris-ltd/midgard-app#status)
[![Stars](https://img.shields.io/github/stars/veldris-ltd/midgard-app?labelColor=12161F&color=CA1D25)](https://github.com/veldris-ltd/midgard-app/stargazers)

</div>

**[`veldris-ltd/midgard-app`](https://github.com/veldris-ltd/midgard-app)** is the sovereign enclosure: an open-source, post-quantum, air-gap-capable platform, published under Apache-2.0. One repository holds the specification (the Solutions Architecture Documents), the design system and the implementation, a Rust workspace with console UIs and a gateway edge.

Midgard Core is the enclosure, the defended trust boundary that provides identity, the object fabric, storage, compute, governance and post-quantum cryptography. Four composable products sit on top of it:

| Product | Domain |
| --- | --- |
| **Midgard** | Core platform: identity, object fabric, governance and the post-quantum cryptography substrate. |
| **Forge** | Data operations: ingest, transform, version and project data into the fabric. |
| **Mimir** | Local agentic AI: on-enclosure inference, grounding, agents and evaluations. No hosted model is ever called. |
| **Bifrost** | Continuous delivery: post-quantum signed artefacts, rollout rings, fleet management and offline bundles. |
| **Heimdall** | Operational fusion: signed feeds, one common operating picture and decision workflows. |

What runs today, and how far each capability goes, is recorded capability by capability in the repository's [claims ledger](https://github.com/veldris-ltd/midgard-app/blob/main/docs/compliance/CLAIMS.md), which CI holds to the source and tests it cites. The authoritative go/no-go record for general availability is [`GA_READINESS.md`](https://github.com/veldris-ltd/midgard-app/blob/main/docs/compliance/GA_READINESS.md). No release has been tagged yet.

**Get started:** [run the design system](https://github.com/veldris-ltd/midgard-app#run-the-design-system) (static files, no toolchain), [run the platform locally](https://github.com/veldris-ltd/midgard-app#run-the-platform-locally), or [verify it](https://github.com/veldris-ltd/midgard-app#verify-the-platform) against the air-gapped acceptance gate.

## Design principles

- **Sovereign by construction.** No core function requires an outbound network call. Midgard runs fully offline and air-gapped, and the acceptance suite proves it under `docker run --network none`.
- **Post-quantum by default.** Hybrid X25519 with ML-KEM-768 in transit. AES-256-GCM at rest under ML-KEM-1024 wrapped keys. ML-DSA and SLH-DSA signatures for service authentication and artefact signing (NIST FIPS 203, 204 and 205). Post-quantum protection is the baseline from version 1.0, never a later upgrade.
- **Local AI native.** Inference runs inside the enclosure, in Mimir.
- **Provenance everywhere.** Every claim has a source and every action has lineage: provenance tags, an append-only post-quantum signed audit ledger and human gates on high-risk actions.
- **Open-source core.** An OSI-approved licence for the core, reproducible builds, vendored dependencies for fully offline builds and a CycloneDX SBOM per release.
- **Evidence over assertion.** Each published capability is backed by a recorded, reproducible gate run, and anything not yet runnable is stated as such.

## Security

Report suspected vulnerabilities privately, never through public issues:

- email [security@veldris.io](mailto:security@veldris.io), or
- use GitHub private vulnerability reporting on [`midgard-app`](https://github.com/veldris-ltd/midgard-app/security) (Security, then Report a vulnerability).

The disclosure policy, timelines and PGP details are in Midgard's [`SECURITY.md`](https://github.com/veldris-ltd/midgard-app/blob/main/SECURITY.md). Veldris Ltd is Cyber Essentials certified.

## Contributing

Contributions to Midgard are welcome. Start with [`CONTRIBUTING.md`](https://github.com/veldris-ltd/midgard-app/blob/main/CONTRIBUTING.md) and [`GETTING_STARTED.md`](https://github.com/veldris-ltd/midgard-app/blob/main/GETTING_STARTED.md). Commits to Veldris repositories are signed, and releases require two-person approval.

## Contact

[veldris.io](https://veldris.io) · [hello@veldris.io](mailto:hello@veldris.io) · [security@veldris.io](mailto:security@veldris.io)

---

<sub>© 2026 Veldris Ltd. Veldris Ltd is registered in England and Wales, company number 17366869. Registered office: Two Snowhill, Birmingham, B4 6WR. ICO registration ZC222667. Midgard source code is licensed under Apache-2.0. Veldris, Midgard and associated product names are the property of Veldris Ltd.</sub>
