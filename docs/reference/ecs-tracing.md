---
mapped_pages:
  - https://www.elastic.co/guide/en/ecs/current/ecs-tracing.html
applies_to:
  stack: all
  serverless: all
---
% This file is automatically generated. Don't edit it manually!

# Tracing fields [ecs-tracing]

Distributed tracing makes it possible to analyze performance throughout a microservice architecture all in one view. This is accomplished by tracing all of the requests - from the initial web request in the front-end service - to queries made through multiple back-end services.

Unlike most field sets in ECS, the tracing fields are *not* nested under the field set name. In other words, the correct field name is `trace.id`, not `tracing.trace.id`, and so on.

## Tracing field details [_tracing_field_details]

| Field | Description | Level |
| --- | --- | --- |
| $$$field-span-id$$$ [span.id](#field-span-id) | Unique identifier of the span within the scope of its trace.<br><br>A span represents an operation within a transaction, such as a request to another service, or a database query.<br><br>type: keyword<br><br>example: `3ff9a8981b7ccd5a`<br><br>![OTel Badge](https://img.shields.io/badge/OpenTelemetry-4a5ca6?style=flat&logo=opentelemetry) [![otlp](https://img.shields.io/badge/OTLP-ffdcb2?style=flat)](/reference/ecs-opentelemetry.md#ecs-opentelemetry-relation) [span_id](https://github.com/search?q=repo%3Aopen-telemetry%2Fopentelemetry-proto+%22\+span_id+%22&type=code) | extended |
| $$$field-trace-id$$$ [trace.id](#field-trace-id) | Unique identifier of the trace.<br><br>A trace groups multiple events like transactions that belong together. For example, a user request handled by multiple inter-connected services.<br><br>type: keyword<br><br>example: `4bf92f3577b34da6a3ce929d0e0e4736`<br><br>![OTel Badge](https://img.shields.io/badge/OpenTelemetry-4a5ca6?style=flat&logo=opentelemetry) [![otlp](https://img.shields.io/badge/OTLP-ffdcb2?style=flat)](/reference/ecs-opentelemetry.md#ecs-opentelemetry-relation) [trace_id](https://github.com/search?q=repo%3Aopen-telemetry%2Fopentelemetry-proto+%22\+trace_id+%22&type=code) | extended |
| $$$field-transaction-id$$$ [transaction.id](#field-transaction-id) | Unique identifier of the transaction within the scope of its trace.<br><br>A transaction is the highest level of work measured within a service, such as a request to a server.<br><br>type: keyword<br><br>example: `00f067aa0ba902b7`<br><br>![OTel Badge](https://img.shields.io/badge/OpenTelemetry-4a5ca6?style=flat&logo=opentelemetry) [![not-applicable](https://img.shields.io/badge/n%2Fa-f2f4fb?style=flat)](/reference/ecs-opentelemetry.md#ecs-opentelemetry-relation) Not applicable. | extended |


