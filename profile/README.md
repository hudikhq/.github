# hudikhq

Home of **[Hoodik](https://hoodik.io)** — lightweight, end-to-end encrypted cloud storage you can run yourself.

Files are encrypted on your device before they leave it; the server only ever stores ciphertext. Even file names and search queries are tokenized and hashed client-side, so whoever operates the server cannot read what you store or what you search for. File keys are wrapped with a quantum-resistant X25519 + ML-KEM-768 hybrid, and login uses OPAQUE, so your password never leaves the device. Every client (web, iOS, Android, macOS) runs the same Rust cryptography, compiled to WASM for the browser and linked natively in the apps.

## Get Hoodik

**Self-host it.** One Docker container, SQLite out of the box (PostgreSQL supported), files on local disk or any S3-compatible bucket. Multi-arch images: amd64, armv6, armv7, arm64.

```shell
docker run --name hoodik -d \
  -e DATA_DIR='/data' \
  -e APP_URL='https://my-app.example.com' \
  --volume "$(pwd)/data:/data" \
  -p 5443:5443 \
  hudik/hoodik:latest
```

Full walkthrough: [self-hosting guide](https://hoodik.io/get-started) · [Docker Hub](https://hub.docker.com/r/hudik/hoodik) · [Unraid templates](https://github.com/hudikhq/hoodik-unraid)

**Or let us run it.** [Hoodik Cloud](https://hoodik.cloud) is a managed instance we operate for you: same code, same end-to-end encryption, no server to maintain. Your data stays as unreadable to us as it would be on your own hardware, and you can export everything and move to self-hosting at any time.

**Get the apps.** [Google Play](https://play.google.com/store/apps/details?id=com.hudikhq.hoodik) · [App Store (iOS and macOS)](https://apps.apple.com/app/hoodik/id6761471179) · [direct APK](https://github.com/hudikhq/hoodik-client/releases) — signed with the same key as the Play build, so either install path updates from the other.

## What it does

- End-to-end encrypted upload, download, and preview, with files split into encrypted chunks for fast concurrent transfers
- Sharing with other users on your server (reader, editor, and co-owner roles, folders included) and read-only public links where the recipient's browser does the decrypting
- Encrypted markdown notes with a WYSIWYG editor
- Search that works without the server ever seeing a plaintext file name or query
- Two-factor authentication and an admin dashboard for users, sessions, and invitations
- Mobile apps with multi-account and multi-server support and offline access

## Repositories

- **[hoodik](https://github.com/hudikhq/hoodik)** — the server and web frontend. Rust (Actix-web) + Vue 3 + WASM crypto. The core of the ecosystem.
- **[hoodik-client](https://github.com/hudikhq/hoodik-client)** — the native client for iOS, Android, and macOS. Flutter over the same Rust crates the web frontend compiles to WASM.
- **[hoodik-unraid](https://github.com/hudikhq/hoodik-unraid)** — container templates for deploying Hoodik on Unraid.

Both the server and the client are licensed [CC BY-NC 4.0](https://github.com/hudikhq/hoodik/blob/master/LICENSE.md): free for personal and non-commercial use, source open for anyone to audit.

## About

Hoodik is developed by **Hudik d.o.o.**, based in Osijek, Croatia. Curious how it compares to Nextcloud, Proton Drive, or Tresorit? See the [comparisons](https://hoodik.io/vs). Bug reports, questions, and contributions are welcome on the individual project repos.
