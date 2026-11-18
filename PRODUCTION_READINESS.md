# Production hardening: Kafka / Spark / Airflow / dbt

**Provenance:** This repository documentation references `ankurchavda/streamify`; distinguish upstream/tutorial code from original contributions before claiming ownership.

## Review and upgrades
- Pin container images, Kafka/Spark/Airflow/dbt versions and dependency hashes.
- Move GCP service account handling from downloaded JSON keys to workload identity / secret manager.
- Replace default Airflow credentials, configure RBAC and remote logs, and enforce HTTPS.
- Set Airflow DAG catchup, retry/backoff, timeout and concurrency explicitly; make ingestion and merge idempotent.
- Validate message schemas, add dead-letter handling and track event-time lag.
- Configure Spark checkpointing, state retention and failure recovery; monitor Kafka consumer lag.
- Add dbt source freshness, uniqueness, not-null and relationship tests; enforce PR validation and deployment approvals.
- Add lineage, dashboards, alerts and an incident runbook.

## Production evidence gate
A successful end-to-end test, reproducible infrastructure deployment, recovery drill and operational SLO evidence are required before calling this production deployed. The repo's README alone does not establish that.
