# Northstar Retail Real-Time Streaming Pipeline

A real-time retail data engineering practical using Microsoft Azure, Azure Event Hubs, Azure Databricks, Apache Spark Structured Streaming and Delta Lake.

## Project Overview

The required practical builds an event-driven retail streaming pipeline:

```text
Azure Virtual Machine
        |
   Event Producer
        |
        v
Azure Event Hubs
        |
   Kafka-compatible stream
        |
        v
Databricks Structured Streaming
        |
        v
Delta Bronze Layer
        |
 Data validation and transformation
        |
        v
Delta Gold Layer
        |
        v
Aggregated retail sales metrics

## Technologies

- Microsoft Azure
- Azure Virtual Machines
- Azure Event Hubs
- Azure Databricks
- Apache Spark and PySpark
- Structured Streaming
- Delta Lake
- Python and Jupyter Notebooks

## Repository Structure

- `data/` — sample CSV files and expected results
- `notebooks/` — main practical and demonstration notebooks
- `scripts/` — project scripts

## Expected Streaming Results

| Metric | Expected |
|---|---:|
| Events produced | 24 |
| Bronze records | 24 |
| Unique sale IDs | 24 |
| Gold aggregation rows | 12 |
| Total transactions | 24 |
| Total quantity | 48 |
| Total revenue | EUR 411.40 |

These are validation targets from the supplied practical, not a claim of fresh execution.

## Checkpoint Recovery

The practical uses separate Bronze and Gold checkpoints to demonstrate recovery from previously recorded streaming progress without restarting the original event producer.

## Optional Extensions

### Azure Data Factory

The optional batch workflow covers file ingestion and Bronze, Silver and Gold processing.

Expected batch targets: 32 source rows, 32 Bronze rows, 24 Silver rows and 4 Gold rows.

### Azure Load Balancer

The optional architecture exercise covers virtual networks, subnets, Network Security Groups, backend pools and health probes.

## Security

- Environment-specific values in the demonstration notebook have been replaced with placeholders.
- Configure your own Azure and Databricks resources before execution.
- Never publish passwords, access keys, tokens or connection strings.
- Local credentials and checkpoints are excluded through `.gitignore`.

## Execution Notes

- Follow the supplied practical instructions.
- Execute notebook cells individually.
- Do not use Run All.
- Complete producer setup before starting streaming.
- Do not resend the original events during checkpoint recovery.
- Record actual observations in the evidence section.

## Execution Status

The repository files and notebooks have been prepared and structurally validated locally. A fresh end-to-end cloud execution is not claimed.

---
