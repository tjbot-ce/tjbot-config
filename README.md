# tjbot-config

Canonical configuration assets for TJBot.

This repository contains the source-of-truth files that define how TJBot is configured:

- `tjbot.default.toml`: documented default runtime configuration
- `tjbot-config.schema.yaml`: JSON Schema used to validate user config
- `model-registry.yaml`: built-in catalog of on-device speech and vision models

These files are used by TJBot's software libraries (e.g. `node-tjbotlib`, `python-tjbotlib`) and by TJBot's bundled configuration editor (`tjbot config`).

## Repository contents

```
.
├── LICENSE
├── model-registry.yaml
├── README.md
├── tjbot-config.schema.yaml
└── tjbot.default.toml
```

## Configuration shape at a glance

Top-level sections in `tjbot.default.toml` and the schema include:

- `log`: runtime log level
- `hardware`: enable/disable attached hardware capabilities
- `listen`: speech-to-text settings (local, IBM, Google, Azure)
- `see`: vision settings (local ONNX, Google, Azure)
- `shine`: LED settings (NeoPixel/Common Anode)
- `speak`: text-to-speech settings (local, IBM, Google, Azure)
- `wave`: servo settings
- `models`: optional user-registered on-device models
- `recipe`: free-form recipe overrides (schema allows additional properties)

## License

Apache-2.0. See `LICENSE`.
