# Measure Studio – Distribution (Development)

This repository is reserved for distributing signed **Measure Studio** desktop preview and stable update packages. **No public release has been published or approved.**

## Current state
- Channel: `preview` (planned, not active)
- Desktop launcher: Rust + Slint
- Accounts and settings: Supabase (separate from this repository)
- Signed manifest: `manifest.json` with detached `manifest.json.sig`
- Artifacts: Windows ZIP packages with SHA-256 hashes
- Public signing key: embedded in the launcher; **private keys must never be committed**

## Planned workflow
1. Build and test on Windows.
2. Generate a signing key **locally, outside the repository**.
3. Embed and pin the public key in the launcher.
4. Create a signed manifest referencing a specific immutable release asset.
5. Validate manifest, signature, download hash, installation, and rollback on a test machine.
6. Only after successful tests, publish preview assets through an explicitly chosen GitHub Release.

**Important:** This repository is public. Do not upload Supabase secrets, private signing keys, test account credentials, personal data, or unfinished client builds.

Development source code is maintained separately. This repo holds distribution material and documentation only.
