# Aether

OpenAPI specs for [podtan/pdt](https://github.com/podtan/pdt) (Platform Data Toolkit).

## Contents

| File | Description |
|------|-------------|
| `pdt-openapi.json` | OpenAPI 3.1 spec for the PDT API — **22 paths**, `info.version: 1.0.0` |

## Source

Fetched from a live PDT server (v0.3.8) at `GET /api-docs/openapi.json`
and committed on 2026-10-18. This spec is fresher than the one checked into
the pdt repo itself (`docs/openapi/pdt-openapi.json`, 17 paths).

## Regenerating

```bash
# start pdt in dev mode
cargo run --features sqlite-backend --bin pdt

# pull the current spec
curl -s http://localhost:8080/api-docs/openapi.json -o pdt-openapi.json
```

## PDT dev mode notes

`AUTH_DEV_MODE=true` injects admin claims into any request that carries no
bearer token — never enable it outside local development.
