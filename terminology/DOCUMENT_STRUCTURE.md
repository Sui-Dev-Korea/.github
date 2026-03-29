# Document Structure

## Purpose

이 문서는 Sui 문서 사이트의 실제 문서 구조를 정리한 참고 문서다.

중요한 기준은 물리적인 폴더명 자체가 아니라, 독자가 실제로 보게 되는 **Docusaurus navbar + sidebar 순서**다.

## Sources

문서 구조는 아래 파일을 기준으로 파악했다.

- `docs/site/docusaurus.config.js`
- `docs/site/sidebars.js`
- `docs/content/sidebars/guides.js`
- `docs/content/sidebars/concepts.js`
- `docs/content/sidebars/standards.js`
- `docs/content/sidebars/references.js`

## Physical Content Roots

실제 문서 파일은 주로 아래 경로에 있다.

- `docs/content/concepts`
- `docs/content/guides`
- `docs/content/standards`
- `docs/content/references`

보조 콘텐츠는 아래 경로에 있다.

- `docs/content/snippets`
- `docs/content/sidebars`

## Top-Level Navigation Order

사이트 navbar 기준 상위 챕터 순서는 다음과 같다.

1. Guides
2. Concepts
3. Standards
4. References

## Detailed Structure

### Guides

1. Overview
2. Getting Started
   - Install Sui
     - Install from source
     - Install binaries
     - Local network
   - Configure Sui Client
   - Get Address
   - Get Coins
   - Hello World
   - App Frontends
   - Next Steps
3. Objects
   - Object Model
   - Types of Object Ownership
     - Address-Owned
     - Immutable
     - Party
     - Shared
     - Wrapped
   - Transfering Objects
     - Custom Rules
     - Transfer Policies
     - Transfer to Object
   - Derived Objects
   - Dynamic Fields
     - Tables and Bags
   - Versioning
   - Local Fee Markets
   - Simulating Refs
4. Packages
   - Package Overview
   - Move Package Management
   - Upgrade
   - Custom Policies
   - Automated Address Management
5. Transactions
   - Transaction Overview
   - Transaction Lifecycle
   - Programmable Transaction Blocks (PTBs)
     - PTB Overview
     - Building PTB
     - Inputs and Results
     - Sign and Send Transaction
   - Transaction Authentication
     - Intent Signing
     - Multisig
     - Offline Signing
     - Address Aliases
   - Sponsored Transactions
   - Gas Smashing
6. Accessing Data
   - gRPC Overview
   - Query with GraphQL
   - Archival Store
   - Using Events
   - Custom Indexing Framework
     - Build
     - Indexer Walrus
     - Bring Your Own Store
7. Currencies and Tokens
   - Currency
   - Address Balances Migration
   - Regulated
   - In-Game Token
   - Loyalty
   - Vesting Strategies
8. NFTs
   - NFT
   - Soulbound NFT
   - Rental NFT
   - Asset Tokenization
9. Wallets
   - SuiLink
10. On-Chain Primitives
   - Access Time
   - Randomness
11. Cryptography
   - Signing
   - Groth16
   - Hashing
   - ECVRF
   - Multisig
   - zkLogin Integration Guide
     - zkLogin
     - zkLogin Integration
     - Developer Account
     - zkLogin Example
12. Nautilus
   - Nautilus Overview
   - Nautilus Design
   - Using Nautilus
   - Customize Nautilus
   - Marlin
   - Seal
13. App Examples
   - E2E Counter
   - Client TS SDK
   - Trustless Swap
   - Coin Flip
   - Reviews Rating
   - Blackjack
   - Plinko
   - Tic-Tac-Toe
   - Oracles
     - Weather Oracle
     - Meta Pricing Oracle
14. Operator Guides
   - Sui Full Node
   - Genesis
   - Monitoring
   - Alerts
   - Updates
   - Data Management
   - Snapshots
   - Archives
   - Exchange Integration
   - Bridge Node Configuration
   - Indexer Stack Setup
   - Archival Stack Setup
   - Remote Store Setup
   - Sui Validator Nodes
15. SuiPlay0X1
   - Integration
   - Migration Strategies
   - Wallet Integration
   - Best Practices
16. Dev Cheat Sheet
17. Move Best Practices
18. Common Errors

### Concepts

1. Overview
2. Sui for Ethereum
3. Sui for Solana
4. Architecture
   - Components
   - Networks
   - Sui Storage
   - Consensus
   - Epochs
   - Sui Security
   - Protocol Upgrades
5. Tokenomics
   - Overview
   - Staking and Unstaking
   - Sui Bridging
   - Gas in Sui
6. Accessing Data
   - gRPC
   - GraphQL RPC
   - Archival Store
   - Custom Indexers
     - Pipeline Architecture
     - Indexer Data Integration
     - Indexer Runtime and Performance
7. Cryptography
   - Passkeys
   - Checkpoint Verification
8. Coin Management
9. Sui Move Concepts
10. Gaming
11. Research Papers

### Standards

1. Overview
2. Coin
3. Currency
4. Closed-Loop Token
   - Action Request
   - Token Policy
   - Spending
   - Rules
   - Coin/Token Comparison
5. Kiosk
6. Kiosk Apps
7. DeepBookV3
   - Design
   - Contract Information
     - Balance Manager
     - Permissionless Pool
     - Query the Pool
     - Orders
     - Swaps
     - Flash Loans
     - Staking Governance
     - Referral
     - EWMA
   - Indexer
   - SDK
     - Balance Manager
     - Pools
     - Orders
     - Swaps
     - Flash Loans
     - Staking Governance
8. DeepBook Margin
   - Design
   - Margin Risks
   - Contract Information
     - Risk Ratio
     - Margin Manager
     - Margin Pool
     - Interest Rates
     - Orders
     - Take Profit / Stop Loss
     - Supply Referral
     - Maintainer
   - Indexer
   - SDK
     - Margin Manager
     - Margin Pool
     - Orders
     - TPSL
     - Maintainer
9. Display
10. Display V2 Migration
11. Payment Kit
12. Sagat
13. Wallet Standard

### References

1. Overview
2. Sui RPC
   - GraphQL
     - Beta
     - Alpha
   - JSON-RPC
   - Fullnode Protocol
   - RPC Best Practices
3. Sui CLI
   - Cheatsheet
   - Client
   - PTB
   - Keytool
   - Move
   - Replay
   - Trace Analysis
   - Validator
4. Sui IDE Support
   - Move
   - Debugger
5. Sui SDKs
   - dApp Kit
   - Rust SDK
   - Rust SDK Reference
   - TypeScript SDK
   - zkSend SDK
6. PTB Commands
7. Move
   - Framework
   - Packages
     - Package Manager Migration
     - Manifest Reference
   - The Move Book
   - The Move Reference
8. Awesome Sui
9. Awesome Sui Gaming
10. Sui Glossary
11. Contribute
   - Sui Environment
   - Contribute to Sui Repos
   - Submit a SIP
   - Localize Sui Docs
   - Code of Conduct
   - Style Guide
   - MDX Components
12. Release Notes

## Reader Order Notes

실제 사이트 노출 순서는 `Guides → Concepts → Standards → References`다.

다만 학습 순서 관점에서는 아래 순서가 더 자연스럽다.

1. Concepts
2. Guides
3. Standards
4. References

## Title and Link Synchronization Notes

이 문서는 제목 번역과 링크 텍스트 번역을 맞추기 위한 기준 맵으로도 사용한다.

- `Detailed Structure`에 나열된 각 페이지를 canonical page unit으로 본다.
- 어떤 페이지 제목을 번역하면, 그 페이지를 가리키는 `title`, `sidebar_label`, `pagination_label`, overview card, 본문 링크 텍스트도 같은 한국어 제목으로 맞춘다.
- 같은 대상 페이지를 찾을 때는 영문 제목만 보지 말고 상대 경로와 챕터 위치를 함께 본다.
- `Overview`, `Design`, `Indexer`, `SDK`, `Orders`처럼 중복되는 제목은 bare title만으로 매칭하지 않는다. 예를 들어 `DeepBookV3 > Indexer`와 `DeepBook Margin > Indexer`는 서로 다른 page unit이다.
- 본문에서 문서 제목을 링크 텍스트로 사용할 때는 가능하면 링크 텍스트를 canonical title 그대로 두고, 조사나 설명은 링크 바깥에 둔다.
- 실제 검색은 현재 문서의 상대 경로와 영문 제목을 함께 사용해 수행한다.

## Translation Planning Notes

번역 우선순위를 잡을 때는 아래 순서를 권장한다.

1. Navbar에 직접 노출되는 상위 개요 페이지
2. `Guides > Getting Started`
3. `Concepts > Architecture`, `Tokenomics`, `Accessing Data`
4. `Guides`의 핵심 개발 경로
5. `Standards`
6. `References`

## Caveats

- 이 문서는 현재 sidebar 설정 기준이다.
- 향후 `docs/content/sidebars/*.js` 또는 `docs/site/docusaurus.config.js`가 바뀌면 구조도 함께 갱신해야 한다.
