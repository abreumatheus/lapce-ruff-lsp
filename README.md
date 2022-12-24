# Ruff LSP for the Lapce editor

## Installing

### Ruff LSP

The ruff-lsp language server must be available on the path. You can install it using the following command:

```bash
pip install ruff-lsp
```

### Editor extension

You can install the extension directly via the Lapce editor, in the extensions tab. Just search for Python (ruff-lsp).

Obs: Don't forget to check the autho's name.

## Configuration

Additional configuration via editor interface will be added in next updates.

## Build

Before building, you must ensure that you have the `wasm32-wasi` target setup.

```shell
rustup target add wasm32-wasi
```

### Debug

```shell
cargo build --target wasm32-wasi
```

### Release

```shell
cargo build --release --target wasm32-wasi
```

## Develop

### OSX / Linux

```shell
cd <lapse_dir>/dev.lapce.Lapce/plugins
```

```shell
mkdir lapce-ruff-lsp

cd lapce-ruff-lsp

ln -s <source_dir>/target/wasm32-wasi/debug/lapce-ruff-lsp.wasm ./bin/
```
