# Changes in this fork

A fork of [reown-com/reown-swift](https://github.com/reown-com/reown-swift) at the `2.4.0` tag, under the same
WalletConnect Community License (see `LICENSE`).

## 2.4.0-macos (2026-10-27)

- `Sources/WalletConnectSign/Auth/Link/LinkEnvelopesDispatcher.swift` imports Foundation and guards its two
  `UIApplication.shared.open` calls with `#if os(iOS)`, so `WalletConnectSign` builds for macOS. Elsewhere Link Mode
  fails with the existing `failedToOpenUniversalLink` error and callers fall back to the relay transport. This is the
  change proposed upstream in reown-com/reown-swift#342 (by andrei-chernikov); nothing else differs from 2.4.0.
