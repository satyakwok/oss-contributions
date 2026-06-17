# Open-source contributions — Satya Kwok

Rust infrastructure engineer. Merged work across the Rust Ethereum stack —
**alloy**, **CometBFT**, and **Foundry** — with active PRs in **Reth**,
**Lighthouse**, and **Agave**. I also build and operate
[**Sentrix Chain**](https://github.com/sentrix-labs/sentrix), a Rust EVM Layer-1.

[satyakwok.dev](https://satyakwok.dev) · [GitHub](https://github.com/satyakwok) · [X @blackskyiee](https://x.com/blackskyiee) · satyakwok88@gmail.com

This is a curated index of upstream contributions. Merged engineering work is listed
first; in-review PRs and Sentrix Chain ecosystem listings are kept separate.

## Merged

### Execution & ABI tooling — alloy / Foundry

- [alloy-rs/core#1122](https://github.com/alloy-rs/core/pull/1122) — validate the event
  topic count before decoding the log body in dyn-ABI, preventing a malformed log from
  being decoded against the wrong topic layout.
- [alloy-rs/core#1124](https://github.com/alloy-rs/core/pull/1124) — propagate
  `extra_derives` to the generated function-call enums in the `sol!` macro, so custom
  derives apply to the call type like they already do to other generated types.
- [alloy-rs/alloy#3976](https://github.com/alloy-rs/alloy/pull/3976) — saturate
  out-of-`u64` `baseFeePerGas` on Ethereum header deserialization instead of failing,
  matching how other oversized numeric fields are handled.
- [foundry-rs/foundry-core#91](https://github.com/foundry-rs/foundry-core/pull/91) —
  preserve base paths in generated block-explorer URLs so sub-path explorer hosts get
  correct links.

### Consensus / BFT — CometBFT

- [cometbft/cometbft#5890](https://github.com/cometbft/cometbft/pull/5890) — proposer
  self-verifies its own vote extension before broadcasting, catching a malformed
  extension locally instead of after it reaches peers.
- [cometbft/cometbft#5861](https://github.com/cometbft/cometbft/pull/5861) — reject
  out-of-int-range float IDs in `idFromInterface` rather than silently truncating them.
- [cometbft/cometbft#5857](https://github.com/cometbft/cometbft/pull/5857) — add
  `LoadValidatorsFast` to skip the proposer-priority advance on the replay path.

## In review

Active upstream PRs in the repositories I want to work in:

- [paradigmxyz/reth#25224](https://github.com/paradigmxyz/reth/pull/25224) — use the
  furthest-reached stage as the pipeline-consistency reference so a stale first stage
  cannot mask execution falling behind headers (relates to #23234).
- [foundry-rs/foundry#15128](https://github.com/foundry-rs/foundry/pull/15128) — return
  a complete `eth_feeHistory` from anvil when the cache lags the chain head.
- [sigp/lighthouse#9435](https://github.com/sigp/lighthouse/pull/9435) — add Unix-domain-socket
  support for the beacon HTTP API.
- [anza-xyz/agave#13076](https://github.com/anza-xyz/agave/pull/13076) — surface
  rollback accounts in fees-only transaction simulation results.
- [alloy-rs/core#1129](https://github.com/alloy-rs/core/pull/1129) — derive `Default`
  for dynamic arrays of non-`Default` elements in the `sol!` macro.
- [alloy-rs/alloy#4040](https://github.com/alloy-rs/alloy/pull/4040) — saturate the base
  fee on the increase path to guard against `u64` overflow.

Plus smaller in-review fixes across Ratatui, XRPL, and candle.

## Sentrix Chain ecosystem listings

Merged registry and integration PRs for [Sentrix Chain](https://github.com/sentrix-labs/sentrix),
the Rust EVM L1 I operate (listed separately from the engineering work above):

- [wevm/viem#4603](https://github.com/wevm/viem/pull/4603) — Sentrix mainnet (7119) and
  testnet (7120) chain definitions.
- [ethereum-lists/chains#8266](https://github.com/ethereum-lists/chains/pull/8266) —
  chain metadata.
- [DefiLlama/chainlist#2707](https://github.com/DefiLlama/chainlist/pull/2707) —
  chainlist entry.
- [DefiLlama/icons#2374](https://github.com/DefiLlama/icons/pull/2374) — icon assets.

## Projects

- [Sentrix Chain](https://github.com/sentrix-labs/sentrix) — Rust EVM Layer-1: native
  Rust node, EVM execution via [`revm`](https://github.com/bluealloy/revm), BFT
  consensus, and full RPC / explorer / faucet / validator tooling.
- [reliakit](https://github.com/satyakwok/reliakit) — zero-dependency Rust reliability
  toolkit (`no_std`-friendly, no `unsafe`): retry/backoff, timeout, rate limiting,
  circuit breaker, bounded collections, secret redaction, health checks.
- [evm-rust-lab](https://github.com/satyakwok/evm-rust-lab) — practical Rust examples
  for Ethereum/EVM workflows with Alloy, REVM, and real RPC.
- [solana-infra-doctor](https://github.com/satyakwok/solana-infra-doctor) — Solana RPC
  readiness diagnostics and redaction-safe reporting in Rust.

## Contact

- Website: https://satyakwok.dev
- GitHub: https://github.com/satyakwok
- X: https://x.com/blackskyiee
- Email: satyakwok88@gmail.com
