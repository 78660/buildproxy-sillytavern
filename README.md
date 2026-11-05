# BuildProxy · 酒馆分流

SillyTavern extension for BuildProxy.

This adapter is derived from the SillyTavern split adapter in
[qiwu622/build-standalone](https://github.com/qiwu622/build-standalone).
It keeps the upstream protocol format (`BUILD_ST_CONTEXT_V1`) so the gateway
can reconstruct the enabled preset inline and put history/background into a
chat attachment.

## Install

SillyTavern → Extensions → Install extension → paste this repository URL.

## Use

- Connection: custom OpenAI-compatible endpoint, or OpenAI with a reverse proxy.
- Endpoint: your BuildProxy gateway, e.g. `http://127.0.0.1:9998/v1`.
- Model: a `build-st/` alias, e.g. `build-st/gemini-4-argon-high`.
- Clear the connection's custom request body and excluded body fields.

The gateway must implement `BUILD_ST_CONTEXT_V1` parsing and the SillyTavern
inline/file context split.

## License and attribution

The adapter code is covered by the Qiwu Noncommercial Attribution License 1.0.
Copyright (c) 2026 qiwu / qiwu622.
Project: https://github.com/qiwu622/build-standalone

Modifications for BuildProxy are identified in this repository.
