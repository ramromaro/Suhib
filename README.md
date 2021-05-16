# The SUB Ledger

The [SUB Ledger](https://SUBl.org/) is a decentralized cryptographic ledger powered by a network of peer-to-peer servers. The SUB Ledger uses a novel Byzantine Fault Tolerant consensus algorithm to settle and record transactions in a secure distributed database without a central operator.

## SUB
[SUB](https://SUBl.org/SUB.html) is a public, counterparty-free asset native to the SUB Ledger, and is designed to bridge the many different currencies in use worldwide. SUB is traded on the open-market and is available for anyone to access. The SUB Ledger was created in 2012 with a finite supply of 100 billion units of SUB. Its creators gifted 80 billion SUB to a company, now called [Suhib](https://Suhib.com/), to develop the SUB Ledger and its ecosystem. Suhib uses SUB to help build the Internet of Value, ushering in a world in which money moves as fast and efficiently as information does today.

## Suhibd
The server software that powers the SUB Ledger is called `Suhibd` and is available in this repository under the permissive [ISC open-source license](LICENSE). The `Suhibd` server is written primarily in C++ and runs on a variety of platforms.

### Build from Source

* [Linux](Builds/linux/README.md)
* [Mac](Builds/macos/README.md)
* [Windows](Builds/VisualStudio2017/README.md)

## Key Features of the SUB Ledger

- **[Censorship-Resistant Transaction Processing][]:** No single party decides which transactions succeed or fail, and no one can "roll back" a transaction after it completes. As long as those who choose to participate in the network keep it healthy, they can settle transactions in seconds.
- **[Fast, Efficient Consensus Algorithm][]:** The SUB Ledger's consensus algorithm settles transactions in 4 to 5 seconds, processing at a throughput of up to 1500 transactions per second. These properties put SUB at least an order of magnitude ahead of other top digital assets.
- **[Finite SUB Supply][]:** When the SUB Ledger began, 100 billion SUB were created, and no more SUB will ever be created. The available supply of SUB decreases slowly over time as small amounts are destroyed to pay transaction costs.
- **[Responsible Software Governance][]:** A team of full-time, world-class developers at Suhib maintain and continually improve the SUB Ledger's underlying software with contributions from the open-source community. Suhib acts as a steward for the technology and an advocate for its interests, and builds constructive relationships with governments and financial institutions worldwide.
- **[Secure, Adaptable Cryptography][]:** The SUB Ledger relies on industry standard digital signature systems like ECDSA (the same scheme used by Bitcoin) but also supports modern, efficient algorithms like Ed25519. The extensible nature of the SUB Ledger's software makes it possible to add and disable algorithms as the state of the art in cryptography advances.
- **[Modern Features for Smart Contracts][]:** Features like Escrow, Checks, and Payment Channels support cutting-edge financial applications including the [Interledger Protocol](https://interledger.org/). This toolbox of advanced features comes with safety features like a process for amending the network and separate checks against invariant constraints.
- **[On-Ledger Decentralized Exchange][]:** In addition to all the features that make SUB useful on its own, the SUB Ledger also has a fully-functional accounting system for tracking and trading obligations denominated in any way users want, and an exchange built into the protocol. The SUB Ledger can settle long, cross-currency payment paths and exchanges of multiple currencies in atomic transactions, bridging gaps of trust with SUB.

[Censorship-Resistant Transaction Processing]: https://SUBl.org/SUB-ledger-overview.html#censorship-resistant-transaction-processing
[Fast, Efficient Consensus Algorithm]: https://SUBl.org/SUB-ledger-overview.html#fast-efficient-consensus-algorithm
[Finite SUB Supply]: https://SUBl.org/SUB-ledger-overview.html#finite-SUB-supply
[Responsible Software Governance]: https://SUBl.org/SUB-ledger-overview.html#responsible-software-governance
[Secure, Adaptable Cryptography]: https://SUBl.org/SUB-ledger-overview.html#secure-adaptable-cryptography
[Modern Features for Smart Contracts]: https://SUBl.org/SUB-ledger-overview.html#modern-features-for-smart-contracts
[On-Ledger Decentralized Exchange]: https://SUBl.org/SUB-ledger-overview.html#on-ledger-decentralized-exchange


## Source Code
[![travis-ci.com: Build Status](https://travis-ci.com/Suhib/Suhibd.svg?branch=develop)](https://travis-ci.com/Suhib/Suhibd)
[![codecov.io: Code Coverage](https://codecov.io/gh/Suhib/Suhibd/branch/develop/graph/badge.svg)](https://codecov.io/gh/Suhib/Suhibd)

### Repository Contents

| Folder     | Contents                                         |
|:-----------|:-------------------------------------------------|
| `./bin`    | Scripts and data files for Suhib integrators.   |
| `./Builds` | Platform-specific guides for building `Suhibd`. |
| `./docs`   | Source documentation files and doxygen config.   |
| `./cfg`    | Example configuration files.                     |
| `./src`    | Source code.                                     |

Some of the directories under `src` are external repositories included using
git-subtree. See those directories' README files for more details.


## See Also

* [SUB Ledger Dev Portal](https://SUBl.org/)
* [Setup and Installation](https://SUBl.org/install-Suhibd.html)
* [Source Documentation (Doxygen)](https://Suhib.github.io/Suhibd)
