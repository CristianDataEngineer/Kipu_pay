# Kipu Pay Lakehouse

Medallion lakehouse on Databricks for Kipu Pay, a Latam payments fintech. Built during my first week as Junior Data Engineer.

## Day 1 - Tuesday 24/11/2026

### Done
- **DE-101**: Kipu workspace set up in Databricks, drop 2026-11-23 landed in a Unity Catalog volume, Git folder connected to GitHub.
- **DE-102**: bronze ingestion for the 6 sources (users, merchants, transactions from 3 files, refunds_chargebacks, fx_rates, app_events), with DDL and ETL split, and row counts in docs/bronze_counts.md.
- **DE-103 (draft)**: top 10 merchants per country for October 2026, by approved TPV in USD. Documented 8 assumptions: period, approved status, dedup by transaction_id, as-of FX join, FX source pending confirmation.

### Found
- Invalid or mixed timestamps
- Inconsistent merchant names (casing, spaces)
- Country codes needing normalization
- Duplicate transaction IDs

### Open
- DE-103: rebuild top 10 on silver (FX conversion for AR/CO broken when computed on raw bronze).
- Lucía: registered users in Chile.