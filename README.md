# CafeLauncher public data mirror

This repository contains the public, generated fallback snapshot used by CafeLauncher when its backend API is unavailable. The backend is the source of truth; this mirror is read-only from the launcher's perspective and may lag behind the latest backend revision.

The mirror worker publishes `mirror-manifest.json` with the profile revisions, file paths, and SHA-256 hashes. The launcher checks the manifest and verifies each payload before using it. The repository contains the current profile JSON, graphics presets, CFG files, and graphics-only history. Published backend release and helper assets appear here only when those artifacts exist.

All repository contents are public, including profile names, settings, and CFG text. Do not put credentials, tokens, or private data in the backend profiles or CFGs. Do not edit generated data files directly; make changes through the backend so its database, manifest, and mirror generation stay consistent.
