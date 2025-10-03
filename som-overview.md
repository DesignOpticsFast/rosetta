# Phoenix System Object Model (SOM) — Overview

- Canonical data model serialized via **Protocol Buffers (proto3)**.
- **Units policy:** preserve declared lens units; all apertures are **diameters**.
- **Copy semantics:** ExecutionCopy and BackupCopy are created by value; EC is for compute only and lives in Bedrock.
- **Tuples:** aperture, field-of-view, focal length, etc., maintain coherent derived values.

## Artifacts
- `/proto/som.proto` (authoritative schema)
- Text form: `.textproto` for human-readable diffs
- Optional export adapters: YAML/JSON for interop

## Responsibilities
- Validate & version SOM
- Provide `SomSnapshot` / `SomDelta` helpers
- Import/export adapters (e.g., ZMX → SOM)
