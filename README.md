# wire-ipc-codex

Codex CLI plugin for Wire IPC — Ed25519 signed outbound messaging between agents.

## Usage

Install via Codex CLI:

```
codex plugin install agiterra/wire-ipc-codex
```

## Configuration

| Env var | Default | Description |
|---|---|---|
| `WIRE_URL` | `http://localhost:9800` | Wire broker URL |
| `WIRE_AGENT_ID` | auto-generated | Agent identifier |
| `WIRE_PRIVATE_KEY` | required | Base64 Ed25519 private key |

`CREW_AGENT_ID` and `CREW_PRIVATE_KEY` override the above when set by the crew launcher.

## What it does

Exposes a `send_message` MCP tool for sending Ed25519-signed IPC messages to other agents via The Wire message broker. Inbound messages are handled by [wire-codex](https://github.com/agiterra/wire-codex).

## Source

- Tools: [@agiterra/wire-ipc-tools](https://github.com/agiterra/wire-ipc-tools)
- Claude Code adapter: [@agiterra/wire-ipc-claude-code](https://github.com/agiterra/wire-ipc-claude-code)
