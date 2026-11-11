# Q3 Campus Energy Audit - Academic Committee Follow-Up Summary

**Committee Meeting:** Academic Committee Meeting
**Date:** November 18, 2026
**Location:** Auditorium B, Main Campus
**Follow-up attachment:** key_findings.pdf (KEY FINDINGS page from campus_energy_audit.pdf)

## Key Findings (from the audit)
- Peak demand down 18% after chiller retrofit
- Solar canopy adds 32 kWh per day
- Night setback saves 4% of baseline load

## Meter Data Load Status
- BigQuery dataset: `facilities_energy` (project `mcp-sync-513611`, location US)
- Table: `meter_readings`
- Source: `meter_readings.csv` (weekly meter export)
- **Readings loaded: 5**
- **Total kWh: 5,630**
- Expected total: 5,630 kWh — **matches; no discrepancies flagged.**

## Data Verification
| Week starting | kWh |
| --- | --- |
| 2026-07-06 | 1180 |
| 2026-07-13 | 1145 |
| 2026-07-20 | 1092 |
| 2026-07-27 | 1104 |
| 2026-08-03 | 1109 |
| **Total** | **5630** |

## Notes
- The `facilities_energy` dataset already existed in the cloud project (created 2026-11-04) and already contained a `meter_readings` table; the local CSV was loaded with WRITE_TRUNCATE to keep it in sync.
- All five weekly readings sum to 5,630 kWh, consistent with the expected export total, so no data-quality flags are required.
