# Coded Estate audit details
- Total Prize Pool: $24,000 in USDT
  - HM awards: $19,700 in USDT
  - QA awards: $800 in USDT
  - Judge awards: $3500 in USDT
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts September 3, 2024 20:00 UTC
- Ends September 17, 2024 20:00 UTC

## This is a Private audit

This audit repo and its Discord channel are accessible to **certified wardens only.** Participation in private audits is bound by:

1. Code4rena's [Certified Contributor Terms and Conditions](https://github.com/code-423n4/code423n4.com/blob/main/_data/pages/certified-contributor-terms-and-conditions.md)
2. C4's [Certified Contributor Code of Professional Conduct](https://code4rena.notion.site/Code-of-Professional-Conduct-657c7d80d34045f19eee510ae06fef55)

*All discussions regarding private audits should be considered private and confidential, unless otherwise indicated.*

Please review the above confidentiality requirements carefully, and if anything is unclear, ask questions in the private audit channel in the C4 Discord.

# Scope

*See [scope.txt](https://github.com/code-423n4/2024-09-coded-estate/blob/main/scope.txt)*

### Files in scope


| File   | Logic Contracts | Interfaces | nSLOC | Purpose | Libraries used |
| ------ | --------------- | ---------- | ----- | -----   | ------------ |

| **Totals** | **** | **** | **undefined** | | |

### Files out of scope

*See [out_of_scope.txt](https://github.com/code-423n4/2024-09-coded-estate/blob/main/out_of_scope.txt)*

| File         |
| ------------ |
| ./contracts/codedestate/src/contract_tests.rs |
| ./contracts/codedestate/src/multi_tests.rs |
| ./packages/cw721/examples/schema.rs |
| Totals: 3 |


# Overview

[ ⭐️ SPONSORS: add info here ]

## Links

- **Previous audits:** None
- **Documentation:** [Coded Estate Playbook](https://coded-estate.gitbook.io/coded-estate)
- **Website:** https://codedestate.com/
- **X/Twitter:** [@codedestate](https://x.com/codedestate)
- **Discord:** https://discord.gg/codedestate

---

# Scope

[ ✅ SCOUTS: add scoping and technical details here ]

### Files in scope
- ✅ This should be completed using the `metrics.md` file
- ✅ Last row of the table should be Total: SLOC
- ✅ SCOUTS: Have the sponsor review and and confirm in text the details in the section titled "Scoping Q amp; A"

*For sponsors that don't use the scoping tool: list all files in scope in the table below (along with hyperlinks) -- and feel free to add notes to emphasize areas of focus.*

| Contract | SLOC | Purpose | Libraries used |  
| ----------- | ----------- | ----------- | ----------- |
| [contracts/folder/sample.sol](https://github.com/code-423n4/repo-name/blob/contracts/folder/sample.sol) | 123 | This contract does XYZ | [`@openzeppelin/*`](https://openzeppelin.com/contracts/) |

### Files out of scope
✅ SCOUTS: List files/directories out of scope

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


## Describe any novel or unique curve logic or mathematical models implemented in the contracts:

None


## Miscellaneous
Employees of Coded Estate and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.
