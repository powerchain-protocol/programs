# PowerChain Programs

PowerChain Programs contains the on-chain Solana programs powering the PowerChain Protocol.

These programs provide decentralized infrastructure for renewable energy assets, real-world assets (RWA), marketplaces, governance, treasury management, staking, rewards, carbon credits, IoT devices, and protocol administration.

---

# Architecture

```
programs/
├── powerchain-core
├── powerchain-governance
├── powerchain-treasury
├── powerchain-marketplace
├── powerchain-rwa
├── powerchain-renewables
├── powerchain-carbon
├── powerchain-rewards
├── powerchain-identity
├── powerchain-oracle
├── powerchain-energy
├── powerchain-iot
├── powerchain-device
├── powerchain-defi
├── powerchain-staking
├── powerchain-bridge
├── powerchain-token
├── powerchain-nft
├── powerchain-vesting
├── powerchain-compliance
└── shared
```

---

# Goals

PowerChain programs are designed to be:

- Modular
- Upgradeable
- Auditable
- Secure
- Permission-aware
- Multi-program
- CPI friendly
- Token-2022 compatible
- Enterprise ready

---

# Workspace

Each program follows the same layout.

```
src/

instructions/
state/
events/
errors/
contexts/
validation/
constants/
utils/

lib.rs
processor.rs
access.rs
security.rs
seeds.rs
```

---

# Core Program

The Core program provides:

- protocol initialization
- configuration
- version management
- registry
- authorities
- feature flags
- pause controls
- CPI helpers

---

# Governance

Responsible for:

- proposals
- voting
- quorum
- execution
- protocol upgrades
- DAO administration

---

# Treasury

Responsible for:

- protocol treasury
- fee collection
- distributions
- reserves
- vaults
- multisig operations

---

# Marketplace

Supports:

- renewable assets
- equipment
- certificates
- NFTs
- tokenized assets
- listings
- purchases
- settlements

---

# Renewable Energy

Supports:

- solar
- wind
- hydro
- geothermal
- battery storage
- production records
- energy certificates

---

# Carbon

Supports:

- carbon projects
- carbon credits
- retirement
- verification
- issuance

---

# RWA

Supports:

- tokenized assets
- ownership
- valuation
- custody
- verification

---

# Rewards

Supports:

- emissions
- staking rewards
- incentive campaigns
- liquidity rewards

---

# Identity

Supports:

- organizations
- operators
- members
- KYC references
- DID integration

---

# IoT

Supports:

- smart meters
- gateways
- telemetry
- production devices
- sensor registration

---

# Faucet

The faucet subsystem supports:

- SPL Token
- Token-2022
- configurable limits
- cooldowns
- per-wallet quotas
- administrator controls
- event logging

---

# Events

Programs emit versioned events for:

- initialization
- updates
- transfers
- settlements
- staking
- rewards
- governance
- faucet claims

---

# Errors

Programs expose consistent error definitions.

Examples include:

- Unauthorized
- InvalidAuthority
- AlreadyInitialized
- InvalidConfiguration
- AccountMismatch
- InsufficientFunds
- InvalidVault
- CooldownActive
- DailyLimitExceeded

---

# Security

PowerChain follows:

- PDA-only authorities
- checked arithmetic
- overflow protection
- replay prevention
- signer verification
- account validation
- CPI validation
- deterministic seeds

---

# Shared Crates

```
crates/

powerchain-core
powerchain-types
powerchain-events
powerchain-errors
powerchain-security
powerchain-utils
powerchain-config
powerchain-sdk
powerchain-math
```

These crates eliminate duplicated logic across programs.

---

# Testing

Testing includes:

- unit tests
- integration tests
- Anchor program tests
- program-test
- local validator
- fuzz testing (recommended)

---

# Build

```bash
cargo fmt

cargo clippy --workspace

cargo test

anchor build

anchor test
```

---

# Deployment

Deploy order:

1. Core
2. Treasury
3. Governance
4. Identity
5. Marketplace
6. Renewables
7. Carbon
8. Rewards
9. Remaining programs

---

# Versioning

Current protocol version:

```
1.0.0-beta.1
```

Programs use semantic versioning and are upgraded through governance where applicable.

---

# Documentation

Additional documentation is available in:

- `/docs`
- `/apps/docs`
- `/packages/powerchain-protocol`
- `/packages/sdk`
- `/docs/architecture`

---

# License

Copyright © PowerChain.

All rights reserved.
