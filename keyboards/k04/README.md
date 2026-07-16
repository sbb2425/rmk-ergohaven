# Ergohaven K:04

No-Qube split BLE firmware for the ordinary K:04 halves.

This target intentionally uses the local legacy RMK 0.8.2 stack:

- `common/rmk-0.8.2-k04`
- `common/rmk-macro-0.7.1-k04`
- `common/rmk-types-0.2.2-k04`

Keep this separate from `keyboards/k04_qube`: the Qube target stays on the root
RMK crates because its dongle connection path is different and works there.

## Build

```sh
cargo build --release --bin central --bin peripheral
```

The repository build matrix also builds this target:

```sh
./scripts/build_k04_matrix.sh
```
