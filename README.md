# Sumo Logic

Sumo Logic is a cloud-native, machine data analytics platform delivering real-time, continuous intelligence for operations, security, and business insights. It provides a comprehensive REST API with 289 endpoints for log analytics, dashboards, monitors, alerts, users, roles, collectors, search jobs, metrics, and traces.

## Links

- [Website](https://www.sumologic.com/)
- [Developer Portal](https://developer.sumologic.com/)
- [API Documentation](https://help.sumologic.com/docs/api/)
- [Interactive API Reference](https://api.sumologic.com/docs/)
- [Getting Started](https://help.sumologic.com/docs/api/about-apis/getting-started/)
- [Status](https://status.sumologic.com)

## APIs

### Sumo Logic API

Base URL: `https://api.{deployment}.sumologic.com/api/` (US1: `https://api.sumologic.com/api/`)

Authentication: HTTP Basic Auth with Access ID and Access Key

**289 endpoints across 54 resource domains including:**
- **Account & User Management** — Users, roles, access keys, SAML, SCIM, password policy
- **Log Analytics** — Search jobs, log searches, extraction rules, parsers, field management
- **Dashboards** — Dashboard creation, panels, and sharing
- **Monitors & Alerts** — Alerting monitors, SLOs, muting schedules
- **Collectors & Sources** — Log collection configuration
- **Content Management** — Folders, content, permissions
- **Metrics** — Metric search, ingest budget management
- **Traces** — Distributed tracing, span analytics, service maps
- **Security** — Threat intelligence, data masking, SOAR connections
- **Apps** — App catalog management

## Artifacts

### OpenAPI

- [sumo-logic-openapi.yml](openapi/sumo-logic-openapi.yml) — Complete OpenAPI 3.0 specification with 289 endpoints

### Spectral Rules

- [sumo-logic-rules.yml](rules/sumo-logic-rules.yml) — Spectral ruleset enforcing Sumo Logic API conventions

### Capabilities

- [log-analytics-observability.yaml](capabilities/log-analytics-observability.yaml) — Workflow capability for log analytics, monitoring, and observability
- [shared/sumo-logic.yaml](capabilities/shared/sumo-logic.yaml) — Per-API shared capability definition

### JSON Schema

- [sumo-logic-user-schema.json](json-schema/sumo-logic-user-schema.json) — JSON Schema for user resources
- [sumo-logic-monitor-schema.json](json-schema/sumo-logic-monitor-schema.json) — JSON Schema for alerting monitors

### JSON Structure

- [sumo-logic-user-structure.json](json-structure/sumo-logic-user-structure.json) — Documented field structure for user resources

### JSON-LD

- [sumo-logic-context.jsonld](json-ld/sumo-logic-context.jsonld) — JSON-LD context mapping Sumo Logic vocabulary to schema.org

### Examples

- [sumo-logic-list-users-example.json](examples/sumo-logic-list-users-example.json) — Example list users request/response
- [sumo-logic-create-monitor-example.json](examples/sumo-logic-create-monitor-example.json) — Example create monitor request/response

### Vocabulary

- [sumo-logic-vocabulary.yml](vocabulary/sumo-logic-vocabulary.yml) — Domain vocabulary for log analytics, observability, and security concepts

## Maintainers

- **Kin Lane** — kin@apievangelist.com
