 ---
title: Changelog
parent: README
nav_order: 1
---# Changelog

## [2.1.8] - 2021-03-04
- Add support for new user configuration options
- Azure fields settings for VPC peering connection refactoring
- Add example initial configuration for GCP Marketplace
- Improve documentation and error messages
- Add empty string validation for OptionalStringToX conversion

## [2.1.7] - 2021-02-11
- Fix `lc_ctype` PostgreSQL database parameter
- Minor documentation improvements

## [2.1.6] - 2021-02-02
- Add Kafka Topic graceful deletion logic
- New Kafka Topic waiter and caching logic, uses v2 endpoint when available.
- Add security policy
- Improve project refresh handling when card id is incorrect
- Uses latest Terraform SDK v2.4.2
- Minor documentation improvements

## [2.1.5] - 2021-01-21
- Add support for renaming projects (only allowed for projects with no powered on services)
- Use latest go-client which fixes Kafka Topic consumer group parsing issue
- Add support for new user configuration options
- Update documentation with the newly available user configuration options
- Kafka topic availability improvements

## [2.1.4] - 2021-01-15
- Improve Kafka Topic caching
- Billing group: change project fields behaviour

## [2.1.3] - 2021-01-11
- Add support for PG upgrade check task
- Use latest go-client version
- Add support for billing groups resource
- Add support for new service user configuration options
- Add support for new service integrations user configuration options
- Use Terraform SDK v2 function instead of deprecated 
- Improve formatting of the code and remove unused functions
- Fix project vpc error handling
- Update service user and service integration documentation
- Fix account team member error handling
- Remove travis ci config

## [2.1.2] - 2020-12-09
- Change VPC peering connection state handling
- Add terraform modules related docs
- Add context support for vpc peering connection
- Add service user new password support
- Extend and improve acceptance tests
- Add project resource diff suppress logic for optional fields
- Add Kafka User Configuration options max values
- Add Redis ACL support to a `service_user` resource
- Fixed docs for mandatory kafka topic params which were marked optional
- Add service integration external user configuration settings

## [2.1.1] - 2020-11-26
- Add new `aiven_project` resource attributes
- Add MirrorMaker examples
- Add new acceptance tests and change settings
- Add support for new user configuration options and service integrations
- Add Terraform version to user agent
- Update Golang requirements
- Add support for GitHub Actions
- Improve service already exists error handling
- Fix kafka topic creation typo
- Fix float to string conversion

## [2.1.0] - 2020-11-16
- Terraform plugin sdk v2 upgrade
- Update documentation: variety of minor updates which includes fix typos / grammar
- Add `is not found` error handling for delete action for all resources
- Add `already exists` error handling for create action for all resources
- Update examples
- Optimise Kafka Topic resource performance
- Fix Kafka Topic empty config issue
- Add example initial configuration for Timescale Cloud
- Add guide for documenting issues encountered during upgrades

## [2.0.11] - 2020-10-27
- Add support for new user configuration options related to Kafka, Kafka Schema Registry, Kafka Connect, Elasticsearch and M3 services.

## [2.0.10] - 2020-10-23
- Fix a bug related to Kafka Topic cache layer
- Small documentation improvements

## [2.0.9] - 2020-10-22
- Add support for M3 DB and M3 Aggregator, these services are currently in beta and available 
only for selected customers; currently, components for both of these services are under development.

## [2.0.8] - 2020-10-20
- Add support for new kafka topic features
- Use go-client v1.5.10
- Improve documentation 
- Add support for new user configuration options
- Simplify certain part of the code 
- Fix Kafka Topic validation since value that is coming from API overflows int

## [2.0.7] - 2020-10-08
- Documentation re-formatting and enhancement
- Temporarily disable docs auto-generation
- Change Kafka Topic resource `retention_hours` behaviour according to API specification
- Use latest go-client version v1.5.9
- Use golang 1.15

## [2.0.6] - 2020-09-23
- Fix README typo in the link to the prometheus/kafka example
- Fix links for kafka schemas example
- Do not change Kafka Schema compatibility level if it is empty or omitted
- Update VPC peering connection documentation

## [2.0.5] - 2020-09-17
- Extend service integration endpoint, add user configuration options
    - `external_aws_cloudwatch_logs`
    - `external_google_cloud_logging`
    - `external_kafka`
    - `jolokia`
    - `signalfx`
- Add support for new user configuration options 
- Add Azure specific behaviour for VPC peering connection resource

## [2.0.4] - 2020-09-11
- Add kafka connector read waiter
- Fix Transit Gateway VPC Attachment Azure fields issue

## [2.0.3] - 2020-09-08
- Extend VPC peering connection creation with new azure related optional fields

## [2.0.2] - 2020-09-04
- Add kafka schema subject compatibility level configuration
- Use go-client v1.5.8
- Add support for -1 user configuration options when min value can be below zero
- Update user configuration options
- Small improvements: fixed tests, formatting and documentation

## [2.0.1] - 2020-08-26
- Add support for service component `aiven_service_component` data source
- Add accounts examples and update documentation
- Add PG example and documentation
- Fix vpc `user_peer_network_cidrs` type conversion problem
- Add support for goreleaser

## [2.0.0] - 2020-08-18
- Migration to Terraform Plugin SDK 0.12
- Add transit gateway vpc attachment documentation
- Add mongo sink connector examples and tests
- Kafka ACL regex modification
- New resources:
    - `aiven_pg` PostgreSQL service 
    - `aiven_cassandra` Cassandra service
    - `aiven_elasticsearch` Elasticsearch service
    - `aiven_grafana` Grafana service
    - `aiven_influxdb` Influxdb service
    - `aiven_redis` Redis service
    - `aiven_mysql` MySQL service
    - `aiven_kafka` Kafka service
    - `aiven_kafka_connect` Kafka Connect service
    - `aiven_kafka_mirrormaker` Kafka Mirrormaker 2 service

## [1.3.5] - 2020-08-11
Add support for transit gateway vpc attachment

## [1.3.4] - 2020-08-10
- Expose new azure config parameters in aiven_vpc_peering_connection resource
- Add support for new user configuration options

## [1.3.3] - 2020-08-06
Fix account team projects resource project reference bug

## [1.3.2] - 2020-07-21
- Force static compilation
- Fix user configuration options array of objects format bug
- Extend elasticsearch acceptance test
- Add support for new user configuration options

## [1.3.1] - 2020-06-30
Improve vpc_id error handling for vpc peering connection

## [1.3.0] - 2020-06-18
- Add support for Kafka Mirrormaker 2 
- User go-client 1.5.5
- User service configuration options refactoring
- Fix Kafka ACL data source
- Add GitHub Pages support
- Add support for Terraform native timeouts
- Add support for Accounts Authentication
- Kafka ACL allow wildcard for username
- Replace Packr2 with go generate 

## [1.2.4] - 2020-05-07
- Speed up kafka topic availability waiter
- Kafka Connect examples
- TF client timings added for the following resources:
    - aiven_vpc_peering_connection
    - aiven_project_vpc
    - aiven_service
    - aiven_kafka_topic

## [1.2.3] - 2020-03-30
Add backwards compatibility for old TF state files created before Kafka `topic` field was renamed to `topic_name`.

## [1.2.2] - 2020-03-10
- Grafana service waits until Grafana is reachable publicly (only works in case `public_access.grafana`
 configuration options is set to `true` and IP filter is set to default `0.0.0.0/0`) during resource creation or update.
- Project VPC resource graceful deletion.

## [1.2.1] - 2020-03-02
Terraform client-side termination protection for resources: 
- aiven_kafka_topic
- aiven_database

## [1.2.0] - 2020-02-18
- Following new types of resources have been added:
     - account
     - account_team
     - account_team_member
     - account_team_project
 
- New configuration options 
- Fix for a read-only replica service types
- Service specific acceptance tests 

## [1.1.6] - 2020-02-07
Fix for a problem that appears for normal boolean user configuration settings

## [1.1.5] - 2020-02-07
Fix for a problem that appears for optional bool user configuration settings

## [1.1.4] - 2020-02-03
- Acceptance tests
- Fix <service>_user_config population problem during import
 
## [1.1.3] - 2020-01-24
Service pg_user_config variant configuration option remove default value.

## [1.1.2] - 2020-01-22
- Fix for <service>_user_config Boolean fields without default value.
- Upgrade golang version to 1.13.
- Allow the API token to be read from an env var.

## [1.1.1] - 2020-01-14
Add VPC Peering Connections `state_info` property

## [1.1.0] - 2020-01-13
Terraform support for Kafka Schema's, Kafka Connectors and Service Components

## [1.0.20] - 2020-01-03
Terraform support for Elasticsearch ACLs

## [1.0.19] - 2019-12-23
Update all service configuration attributes to match latest definitions.

## [1.0.18] - 2019-12-09
Enable Kafka topics caching and add support of the Aiven terraform plugin on Windows

## [1.0.17] - 2019-09-16
Do not explicitly wait for Kafka auxiliary services to start up in an
attempt to fix issues with Kafka service create operation timing out.

## [1.0.16] - 2019-09-02
Update all service configuration attributes to match latest
definitions.

## [1.0.15] - 2019-08-19
Switch to using packr v2

## [1.0.14] - 2019-08-16
Datasource support

## [1.0.13] - 2019-08-12
Handle API errors gracefully during Kafka topic creation.

## [1.0.12] - 2019-08-08
Always wait for VPC state to become active before treating it as created.
Mark more URIs as sensitive.

## [1.0.11] - 2019-08-06
Suppress invalid update when maintenance window is unset.
Handle lc_collate and lc_ctype database attributes better.
Report Terraform provider version to server.
Treat service_uri as sensitive to avoid showing password in plain text.
Fix importing existing aiven_database resource.
Support external Elasticsearch integration.
Update available advanced configuration options.

## [1.0.10] - 2019-06-10
Switch to using go.mod
Support cross-region VPC Peering.

## [1.0.9] - 2019-04-26
Build with CGO_ENABLED=0.

## [1.0.8] - 2019-04-03
Wait for VPC to reach active state before creating service.
Don't wait for Kafka aux services if network restrictions may apply.

## [1.0.7] - 2019-03-29
Support managing MySQL services. Update all service and integration
configuration attributes match latest definitions from server.

## [1.0.6] - 2019-03-11
Fix service_port type to make it properly available.
Use latest service info on create/update to make service specific
connection info available.

## [1.0.5] - 2019-02-05
Improve retry logic in some error cases.

## [1.0.4] - 2019-01-07
Fix service_username property for services.

## [1.0.3] - 2018-12-11
Ensure Kafka topic creation succeeds immediately after service creation.
Support setting service maintenance window.
Provide cloud provider's VPC peering connection ID (AWS only).

## [1.0.2] - 2018-11-21
Support for Prometheus integration and some new user config values.

## [1.0.1] - 2018-10-08
Support termination_protection property for services.

## [1.0.0] - 2018-09-27
Support all Aiven resource types. Also large changes to previously
supported resource types, such as full support for all user config
options.

**NOTE**: This version is not backwards compatible with older versions.
