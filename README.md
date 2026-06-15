# Mantle Messenger Contracts

Solidity contracts for the Mantle Private Messenger protocol.

This repository is the canonical on-chain protocol layer for the messenger.

The TypeScript SDK package @mantle/messenger-core is built specifically for these contracts:
https://github.com/kostiksobol/mantle-messenger-core

## What is included

- MainConnector user registry and protocol entrypoint
- messenger user/profile contract logic
- chat/message/invitation on-chain protocol contracts
- Foundry scripts and tests

## Build

    forge build

## Test

    forge test

## Relationship with messenger-core

@mantle/messenger-core contains the TypeScript protocol/client layer:

- ABI usage
- local database sync
- encryption helpers
- messenger write actions
- transaction layer abstraction

This repository contains the Solidity source of the protocol that messenger-core expects.

When contracts change, the ABI/types used by messenger-core must be updated to match the deployed MainConnector.
