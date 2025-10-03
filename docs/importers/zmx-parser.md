# ZMX Importer Pipeline (Rosetta)

## Pipeline
1. Read UTF‑16 text, tokenize lines
2. Parse **units, environment, wavelengths, fields**
3. Parse surface table and stop designation
4. Construct `SystemModel` with an **Intended Path**
5. Mark the stop surface; convert semi‑diameters → diameters
6. Produce a validated SOM snapshot

## Notes
- Stop surface: only one allowed; defaults to first face in Intended Path if unspecified.
- Height-based fields use lens units; wavelengths stored in microns.
