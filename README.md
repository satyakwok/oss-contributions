# OSS Contributions

I am Satya Kwok. As an external contributor, I work on open-source infrastructure across Rust, Ethereum/EVM tooling, consensus systems, and developer tooling.

This repository is a curated index of selected upstream contributions.

## Highlights

- Rust and Ethereum infrastructure
- ABI and EVM tooling correctness
- Ethereum header, RPC, and block-explorer correctness
- Consensus / BFT infrastructure
- Ecosystem integrations

## Merged contributions

### Rust / Ethereum infrastructure

- [alloy-rs/core#1122](https://github.com/alloy-rs/core/pull/1122) — validate event topic count before decoding the log body in dyn-ABI.
- [alloy-rs/core#1124](https://github.com/alloy-rs/core/pull/1124) — propagate `extra_derives` to generated function-call enums in the `sol!` macro.
- [alloy-rs/alloy#3976](https://github.com/alloy-rs/alloy/pull/3976) — fix Ethereum header deserialization for out-of-`u64` `baseFeePerGas` values.
- [foundry-rs/foundry-core#91](https://github.com/foundry-rs/foundry-core/pull/91) — preserve base paths in generated block-explorer URLs.

### Consensus / blockchain infrastructure

- [cometbft/cometbft#5890](https://github.com/cometbft/cometbft/pull/5890) — consensus: proposer self-verifies its own vote extension before broadcast.
- [cometbft/cometbft#5861](https://github.com/cometbft/cometbft/pull/5861) — rpc/jsonrpc: reject out-of-int-range float IDs in `idFromInterface`.
- [cometbft/cometbft#5857](https://github.com/cometbft/cometbft/pull/5857) — consensus: add `LoadValidatorsFast` to skip proposer-priority advance.

### Ecosystem integrations

- [wevm/viem#4603](https://github.com/wevm/viem/pull/4603) — add Sentrix Chain mainnet/testnet chain definitions.
- [ethereum-lists/chains#8266](https://github.com/ethereum-lists/chains/pull/8266) — add Sentrix Chain metadata.
- [DefiLlama/chainlist#2707](https://github.com/DefiLlama/chainlist/pull/2707) — add Sentrix Chain to chainlist.
- [DefiLlama/icons#2374](https://github.com/DefiLlama/icons/pull/2374) — add Sentrix Chain icon assets.

## Active upstream work

In-review upstream PRs and investigations across Rust and Ethereum infrastructure — Reth, Foundry, Alloy, Lighthouse, Ratatui, XRPL, Solana (Agave), and Bevy. These are ongoing and not counted as merged work.

## Related work

- [Sentrix Chain](https://github.com/sentrix-labs/sentrix) — Rust-based EVM Layer-1 blockchain infrastructure.
- [reliakit](https://github.com/satyakwok/reliakit) — reliability toolkit for Rust CLIs, services, bots, and infrastructure tools.
- [evm-rust-lab](https://github.com/satyakwok/evm-rust-lab) — practical Rust examples for Ethereum/EVM workflows.
- [solana-infra-doctor](https://github.com/satyakwok/solana-infra-doctor) — Solana RPC readiness diagnostics and infrastructure checks in Rust.

## Contact

- GitHub: https://github.com/satyakwok
- Website: https://satyakwok.dev
- X: https://x.com/blackskyiee
- Email: satyakwok88@gmail.com
