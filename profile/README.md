# hudikhq

Home of **[Hoodik](https://hoodik.io)** — a lightweight, self-hosted, end-to-end encrypted cloud storage system. Files are encrypted in your browser before they ever leave your device; the server never sees plaintext data.

## Projects

- **[hoodik](https://github.com/hudikhq/hoodik)** — the server and web frontend. Rust (Actix-web) + Vue 3 + WASM crypto. The open-source core of the ecosystem.
- **[hoodik-landing](https://github.com/hudikhq/hoodik-landing)** — source of the marketing site at [hoodik.io](https://hoodik.io). Nuxt 3.
- **[hoodik-unraid](https://github.com/hudikhq/hoodik-unraid)** — container templates for deploying Hoodik on Unraid.

Native apps for iOS, Android, macOS, Windows, and Linux are built on top of the same Rust crates as the server, so every client shares the same audited cryptography.

## Try it

- **Website:** [hoodik.io](https://hoodik.io)
- **Docker images:** [hudik/hoodik](https://hub.docker.com/r/hudik/hoodik) (multi-arch: amd64, armv6, armv7, arm64)
- **VPS setup guide:** [hoodik.io/get-started](https://hoodik.io/get-started)
- **Android app:** [Google Play](https://play.google.com/store/apps/details?id=com.hudikhq.hoodik)

## About

Hoodik is developed by **Hudik d.o.o.**, based in Osijek, Croatia. Bug reports, questions, and contributions are welcome on the individual project repos.
