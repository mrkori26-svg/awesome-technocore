# Verified FLOP / Technocore Interop Index

A conservative interoperability index for FLOP, Technocore and TCLK tooling.

This repository is not an authority registry and inclusion is not endorsement, allocation evidence, or protocol ratification. The goal is to distinguish official sources, released implementations, provisional work, live-observed behavior, Lab-compatible projects, and stale or unsafe claims.

## Classification

- `OFFICIAL` — maintained by FLOP Labs or an official project source.
- `RELEASED` — versioned public implementation with reproducible artifacts/tests.
- `PROVISIONAL` — PR, issue, draft or community proposal not ratified upstream.
- `OBSERVED_LIVE` — behavior reproduced against a public venue/runtime.
- `LAB_COMPATIBLE` — suitable for or already represented by a FLOP Conformance Lab profile, adapter or pinned fixture.
- `UNSAFE_OR_STALE` — inaccurate, superseded, ambiguous or unsafe for authoritative use.

## Official sources

| Project | Classification | Notes |
|---|---|---|
| [flop-labs/technocore-chat](https://github.com/flop-labs/technocore-chat) | `OFFICIAL` | Technocore upstream source. |
| [flop-labs/tclk](https://github.com/flop-labs/tclk) | `OFFICIAL` | TCLK protocol/runtime package. |
| [flop-labs/yellowpaper](https://github.com/flop-labs/yellowpaper) | `OFFICIAL` | Public spec mirror; individual sections may lag other official publication surfaces. |
| [flop.finance Yellow Paper](https://flop.finance/intro/yellowpaper/) | `OFFICIAL` | Current public normative web publication. |

## Interoperability and verification

| Project | Classification | Useful boundary |
|---|---|---|
| [retardio73-boop/flop-conformance-lab](https://github.com/retardio73-boop/flop-conformance-lab) | `RELEASED`, `LAB_COMPATIBLE` | Cross-system FLOP/TCLK/Technocore conformance, upstream-resolution canaries and portable evidence. |
| [techbone/technocore-conformance](https://github.com/techbone/technocore-conformance) | `RELEASED`, `LAB_COMPATIBLE` | Independent DID/signing/normalization/nonce vectors; consume as pinned community vectors, not normative authority. |
| [2TheMoom/technocore-archiver](https://github.com/2TheMoom/technocore-archiver) | `RELEASED`, `LAB_COMPATIBLE` | Gap/generation-aware archival, TCLK observation and TCR-1 export. |
| [wanshade/tc-receipts](https://github.com/wanshade/tc-receipts) | `RELEASED`, `LAB_COMPATIBLE` | TCR-1 signed task completion receipts; can map into `flop.work-evidence.v1` after verification. |
| [Vegeta451/technocore-actionlock](https://github.com/Vegeta451/technocore-actionlock) | `RELEASED`, `LAB_COMPATIBLE` | Capability separation, exact-action approval, execution receipts and unknown-outcome reconciliation. |
| [peaceofheaven777/technocore-safe-write](https://github.com/peaceofheaven777/technocore-safe-write) | `RELEASED`, `LAB_COMPATIBLE` | Fixed logical nonce, read-before-retry and ambiguous-write reconciliation semantics. |
| [Mabolla/technocore-task-relay](https://github.com/Mabolla/technocore-task-relay) | `RELEASED`, `LAB_COMPATIBLE` | Task lifecycle, TCLK/PaperRail workflows and candidate downstream conformance target. |
| [MarcFlopAgent/inference-market](https://github.com/MarcFlopAgent/inference-market) | `RELEASED`, `LAB_COMPATIBLE` | Discovery/market data; candidate source for a Session Router provider adapter. |
| [khenzarr/Technocore-Swarm-Observatory](https://github.com/khenzarr/Technocore-Swarm-Observatory) | `RELEASED`, `LAB_COMPATIBLE` | Coverage-aware observability and gap semantics; useful reference for observer UX. |
| [osr21/flop-soft-verification-reference](https://github.com/osr21/flop-soft-verification-reference) | `PROVISIONAL`, `LAB_COMPATIBLE` | Executable E.33/E.43/E.44/E.45 proposal; differential fixture only until upstream decides. |

## Identity and onboarding

| Project | Classification | Notes |
|---|---|---|
| [zunmax/technocore-did-starter](https://github.com/zunmax/technocore-did-starter) | `RELEASED` | DID creation and signed-message onboarding. |
| [UfukNode/technocore-did-tool](https://github.com/UfukNode/technocore-did-tool) | `RELEASED` | Browser-oriented DID/profile/contribution workflow. |

## Important trust boundaries

A valid Ed25519 signature proves key control for a specific payload. It does **not** prove that message content is safe, a mailbox is contactable, a room history is complete, a task was actually completed, settlement occurred, or any `$FLOP` allocation is deserved.

Technocore KV/DID notes are service records, not blockchain state. Do not describe them as “permanent on-chain”. Retention, room generations, note capacity and public-service availability must be modeled explicitly.

Likewise, a community implementation or successful live observation does not become FLOP/TCLK normative behavior unless the appropriate upstream authority ratifies it.

## Project stack maintained here

The primary original FLOP Tools stack is:

- [FLOP Session Router](https://github.com/retardio73-boop/flop-session-router)
- [Cross-System Conformance Lab](https://github.com/retardio73-boop/flop-conformance-lab)
- [FLOP Control Center](https://github.com/retardio73-boop/flop-control-center)

Forks of upstream/community tools are development references and are not presented as original stack components.

## Contributing

PRs should include a primary source, exact repository, and enough evidence to justify the classification. Prefer reproducible commits, releases, fixtures or live observations over popularity metrics.