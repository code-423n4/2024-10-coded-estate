# Coded Estate audit details
- Total Prize Pool: $29,400 in USDT
  - HM awards: $23,500 in USDT
  - QA awards: $1,000 in USDT
  - Judge awards: $4,400 in USDT
  - Scout awards: $500 in USDT
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts October 4, 2024 20:00 UTC
- Ends October 11, 2024 20:00 UTC

## This is a Private audit

This audit repo and its Discord channel are accessible to **certified wardens only.** Participation in private audits is bound by:

1. Code4rena's [Certified Contributor Terms and Conditions](https://github.com/code-423n4/code423n4.com/blob/main/_data/pages/certified-contributor-terms-and-conditions.md)
2. C4's [Certified Contributor Code of Professional Conduct](https://code4rena.notion.site/Code-of-Professional-Conduct-657c7d80d34045f19eee510ae06fef55)

*All discussions regarding private audits should be considered private and confidential, unless otherwise indicated.*

Please review the above confidentiality requirements carefully, and if anything is unclear, ask questions in the private audit channel in the C4 Discord.


# Overview

At its essence, Coded Estate is a pioneering decentralized platform that serves as an all in one hub for potential buyers and sellers and a bridge for travelers seeking unique experiences. Through an intuitive interface, homeowners can mint their properties into dynamic NFTs, enabling effortless rental revunue, APY and transfer on the blockchain.                          

Coded Estate introduces the transformative benefit of fractionalized ownership, allowing users to invest in portions of real estate assets, democratizing property investments and ensuring broader participation. Additionally, the platform harnesses the power of AI, providing tailored recommendations, enhanced atutomation without intermediaries and investment insights to users, ensuring they make informed decisions.

Consumers can explore and purchase homes or indulge in vacation retreats, transacting smoothly in digital currency, empowered by smart contracts and Coded Estate's combination of cutting edge- technologies.

## Links

- **Previous audits:** None
- **Documentation:** [Coded Estate Playbook](https://coded-estate.gitbook.io/coded-estate)
- **Website:** https://codedestate.com/
- **X/Twitter:** [@codedestate](https://x.com/codedestate)
- **Discord:** https://discord.gg/codedestate

---

# Scope

### Files in scope

*See [scope.txt](https://github.com/code-423n4/2024-09-coded-estate/blob/main/scope.txt)*


| File                                       | blank | comment | code |
|--------------------------------------------|-------:|--------:|-----:|
| contracts/codedestate/src/execute.rs       | 172   | 154     | 1198 |
| contracts/codedestate/src/query.rs         | 41    | 15      | 376  |
| ./packages/cw721/examples/schema.rs |   |  | 1678 |
| contracts/codedestate/src/msg.rs           | 31    | 99      | 182  |
| packages/cw721/query.rs                    | 24    | 48      | 167  |
| contracts/codedestate/src/state.rs         | 28    | 26      | 162  |
| contracts/codedestate/src/helpers.rs       | 19    | 8       | 163  |
| packages/cw721/traits.rs                   | 23    | 3       | 148  |
| contracts/codedestate/src/lib.rs           | 23    | 15      | 95   |
| contracts/codedestate/src/error.rs         | 22    | 0       | 50   |
| packages/cw721/receiver.rs                 | 5     | 5       | 31   |
| packages/cw721/msg.rs                      | 1     | 10      | 24   |
| packages/cw721/lib.rs                      | 2     | 0       | 14   |

### Files out of scope

*See [out_of_scope.txt](https://github.com/code-423n4/2024-09-coded-estate/blob/main/out_of_scope.txt)*


| File         |
| ------------ |
| ./contracts/codedestate/src/contract_tests.rs |
| ./contracts/codedestate/src/multi_tests.rs |
| Totals: 2 |


## Scoping Q &amp; A

### General questions

| Question                                | Answer                       |
| --------------------------------------- | ---------------------------- |
| ERC20 used by the protocol              | Any (all possible ERC20s)     |
| ERC721 used  by the protocol            | Real estate nft              |
| ERC777 used by the protocol             | No                           |
| ERC1155 used by the protocol            | No                           |
| Chains the protocol will be deployed on | Nibiru Blockchain            |

### ERC20 token behaviors in scope

| Question                                                                                                                                                   | Answer |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Missing return values](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#missing-return-values)                                                      | Out of scope  |
| [Fee on transfer](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#fee-on-transfer)                                                                  | Out of scope  |
| [Balance changes outside of transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#balance-modifications-outside-of-transfers-rebasingairdrops) | Out of scope  |
| [Upgradeability](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#upgradable-tokens)                                                                 | Out of scope  |
| [Flash minting](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#flash-mintable-tokens)                                                              | Out of scope  |
| [Pausability](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#pausable-tokens)                                                                      | Out of scope  |
| [Approval race protections](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#approval-race-protections)                                              | Out of scope  |
| [Revert on approval to zero address](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-approval-to-zero-address)                            | Out of scope  |
| [Revert on zero value approvals](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-approvals)                                    | Out of scope  |
| [Revert on zero value transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-transfers)                                    | Out of scope  |
| [Revert on transfer to the zero address](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-transfer-to-the-zero-address)                    | Out of scope  |
| [Revert on large approvals and/or transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-large-approvals--transfers)                  | Out of scope  |
| [Doesn't revert on failure](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#no-revert-on-failure)                                                   | Out of scope  |
| [Multiple token addresses](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-transfers)                                          | Out of scope  |
| [Low decimals ( < 6)](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#low-decimals)                                                                 | Out of scope  |
| [High decimals ( > 18)](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#high-decimals)                                                              | Out of scope  |
| [Blocklists](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#tokens-with-blocklists)                                                                | Out of scope  |

### External integrations (e.g., Uniswap) behavior in scope:


| Question                                                  | Answer |
| --------------------------------------------------------- | ------ |
| Enabling/disabling fees (e.g. Blur disables/enables fees) | No     |
| Pausability (e.g. Uniswap pool gets paused)               | No     |
| Upgradeability (e.g. Uniswap gets upgraded)               | No     |


# Additional context

## Main invariants

Anybody can mint his real estate NFT, and he has full access to manage it

## Attack ideas (where to focus for bugs)

None


## All trusted roles in the protocol

None

## Building
Install Rust version 1.72.1 and then run `cargo build`


## Describe any novel or unique curve logic or mathematical models implemented in the contracts:

None


## Miscellaneous
Employees of Coded Estate and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.
