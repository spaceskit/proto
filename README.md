# @spaceskit/proto

Shared Protocol Buffer definitions for the Spaceskit coordination protocol.

`proto/` is the canonical cross-process contract source of truth. Generated
consumer artifacts are emitted into `gateway/packages/contracts/src/generated`.

## Structure

```
proto/spaceskit/v2/
├── common.proto                 # Shared enums, messages
├── integration_service.proto    # Integration catalog + request intake
├── runtime_service.proto        # Runs, run steps, approvals, artifacts
├── space_service.proto          # Space lifecycle, agent provisioning
├── coordinator_service.proto    # Turn orchestration, feedback routing
├── profile_service.proto        # Agent profiles, revisions, insights
├── experience_service.proto     # Experience generation & curation
├── capability_service.proto     # Capability management
├── skill_service.proto          # Skills & actions
├── speech_service.proto         # Speech I/O
├── event_stream.proto           # Trace events
├── health_service.proto         # Health/status reporting
├── usage_service.proto          # Runtime policy, behavior, usage snapshots
├── gateway_service.proto        # Gateway-wide policy management
├── scheduler_service.proto      # Gateway scheduler jobs and run history
└── sync_service.proto           # Gateway-to-gateway sync
```

## Usage

These definitions are consumed by:

- **spaceskit/gateway** — TypeScript reference implementation
- **spaceskit/client-swift** — Swift client library
- **spaceskit/client-ts** — TypeScript client SDK

## Code Generation

```bash
buf generate
```

## License

See [LICENSE](./LICENSE).
