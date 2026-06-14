# Sumo Logic GraphQL Schema

This directory contains a conceptual GraphQL schema for the Sumo Logic cloud logging and monitoring platform, derived from the [Sumo Logic REST API v1](https://api.sumologic.com/docs/).

## Overview

Sumo Logic provides a cloud-native machine data analytics platform with a comprehensive REST API covering log analytics, dashboards, monitors, roles, users, metrics, traces, and more. This GraphQL schema represents the core domain model as a typed graph, enabling flexible querying across collectors, sources, searches, dashboards, monitors, alerts, and administrative resources.

## Schema File

- [sumo-logic-schema.graphql](sumo-logic-schema.graphql)

## Type Categories

### Collector Types
- `HostedCollector` — Cloud-based collector managed by Sumo Logic
- `InstalledCollector` — Agent installed on a host machine

### Source Types
- `Source` — Base source attached to a collector
- `SourceDetails` — Extended source with all configuration fields
- `HTTPSource` — Ingests data via HTTP/HTTPS endpoint
- `S3Source` — Reads logs from Amazon S3 buckets
- `CloudFront` — Reads Amazon CloudFront access logs from S3
- `SyslogSource` — Collects syslog messages over UDP/TCP
- `WindowsEventSource` — Collects Windows Event Log entries

### Log Types
- `LogField` — Key-value metadata field attached to log data
- `LogMetadata` — Source and collector context for a log entry
- `LogEntry` — A single log message with parsed fields and metadata
- `ParsedMessage` — Log message with extracted key-value fields

### Search Types
- `SearchQuery` — Input parameters for a log search
- `SearchJob` — Asynchronous search job with lifecycle state
- `SearchJobDetails` — Full details including counts and histogram buckets
- `SearchJobStatus` — Current state and counts for a running job
- `SearchMessages` — Paginated log messages from a completed search
- `SearchRecord` — A single aggregation record from a search
- `SearchAggregation` — Collection of aggregation records with field definitions

### Metrics Types
- `TimeSeries` — A named metric with dimensional labels and data points
- `MetricDataPoint` — A single timestamp-value pair in a time series
- `MetricsQuery` — A metrics query row with rollup configuration
- `MetricsResult` — Query results grouping time series by row ID

### Dashboard Types
- `Dashboard` — Summary view of a dashboard resource
- `DashboardDetails` — Full dashboard with panels and variables
- `Panel` — Summary panel descriptor
- `PanelDetails` — Full panel with queries, chart type, and visual settings
- `PanelChartType` — Enum of supported visualization types

### Monitor Types
- `Monitor` — Summary view of a monitor
- `MonitorDetails` — Full monitor with triggers and notifications
- `MonitorStatus` — Enum of operational states (NORMAL, CRITICAL, WARNING, etc.)
- `MonitorCondition` — Trigger condition threshold and window configuration
- `MonitorQuery` — Query row tied to a monitor

### Alert Types
- `AlertGroup` — Grouped set of alerts from a monitor
- `AlertDetails` — Individual alert with start/end times and resolution info
- `AlertSummary` — Aggregated counts by severity
- `AlertConnection` — Webhook connection for alert delivery
- `AlertWebhook` — Individual webhook endpoint with method and payload

### Content and Folder Types
- `Folder` — Container for organizing dashboards, searches, and reports
- `Content` — Generic content item within the library

### Report Types
- `Report` — Scheduled report with template and delivery configuration
- `ReportSchedule` — Frequency, time, and recurrence settings
- `ReportDelivery` — Recipient list and format (PDF, PNG, CSV)

### User and Role Types
- `User` — Summary user record with role assignments
- `UserDetails` — Full user with MFA status and last login time
- `UserRole` — Association between a user and a role
- `Role` — Named role with capabilities and filter predicate
- `Permission` — Access grant linking a role or user to content

### Organization Type
- `Organization` — Top-level account with tier, credits, and limits

### Partition Types
- `PartitionDetails` — Log partition with routing expression and retention
- `PartitionInfo` — Summary partition stats including byte count
- `Field` — Custom log field with name, data type, and state

### Auth Types
- `Token` — Session or service token
- `APIKey` — Access ID/key pair for API authentication

### Infrastructure Types
- `RateLimitInfo` — Per-minute and per-hour quota consumption

## Reference

- REST API Docs: https://api.sumologic.com/docs/
- Developer Portal: https://developer.sumologic.com/
- Help Center: https://help.sumologic.com/docs/api/
- GitHub: https://github.com/SumoLogic
