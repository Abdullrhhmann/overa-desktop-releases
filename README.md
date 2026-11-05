# Overa desktop releases

This repository holds **releases only**: the Overa desktop app's installers (NSIS `-setup.exe`),
the MSI for IT, their update signatures, and the update manifests. It never holds source code.

- **Channels:** the release `channel-test` carries the test channel's `latest.json`, and
  `channel-stable` the stable channel's. An installed app reads only its own channel's manifest,
  so a pre-release never reaches a PC on the stable channel.
- **Versions:** each version is its own release (`v0.9.0`, `v0.9.0-test.1`...). Test builds are
  marked as pre-releases.
- **Signatures:** every update is signed with the publisher's Ed25519 key, and the app refuses a
  file whose signature does not match the public key built into it. A changed file here is harmless.
