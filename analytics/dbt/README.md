# Analytics overlays for Kanban template

This directory carries dbt metadata (exposures) so customer repositories can publish
Flow health dashboards alongside code. The core dbt project still lives in the main
Kiket repo (`analytics/dbt/`), but keeping the exposure definition here ensures the
metrics show up in docs builds when this template repo is the root project.

- `exposures/flow_health.yml` documents the Flow Health dashboard and its
  dependencies (`fct_throughput`, `fct_cycle_time`, `fct_usage_events`).

When cloning this repository as a starting point, ensure the main application dbt
project is available on the execution runner so the exposure can be compiled.
