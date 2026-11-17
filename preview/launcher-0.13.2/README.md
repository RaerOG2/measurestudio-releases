# Measure Studio Launcher 0.13.2 — preview staging

**Development only. This is NOT a GitHub Release and NOT a compiled Windows installer.**

This directory describes the 0.13.2 delta patch, which applies to a complete local 0.13.1 Rust/Slint workspace. The original ZIP is available in the corresponding ChatGPT development conversation and is **not yet uploaded to GitHub**.

## Patch metadata
- Version: `0.13.2`
- Package: `measurestudio-launcher-preview-0.13.2-update-center-stability.zip`
- Size: `27044` bytes
- SHA-256: `37ef1728b31aa26217c2a4f20b2764f991dc3c5dab0fc0c42cf79f8a908b22dc`
- Contains seven files: launcher source, release channel and updater modules, Cargo configuration, and release notes.
- Preview channel only. Never publish private signing keys.

## Next steps on a Windows development machine
1. Merge the 0.13.2 delta ZIP into the existing 0.13.1 workspace.
2. Run `cargo test -p measurestudio-msreleasechannel`, `cargo test -p measurestudio-msupdater`, and `cargo check -p measurestudio-launcher`.
3. Run the signed updater E2E script against a separate sandbox installation.
4. Build the Windows package and sign an immutable release manifest with the local private signing key.
5. Upload the tested Windows ZIP and detached manifest/signature to a **GitHub pre-release** only when explicitly approved.

**Do not point the active launcher update channel to this branch.** A GitHub branch file is not a signed software release.
