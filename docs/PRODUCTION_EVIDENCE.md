# Production Evidence — Recorded Snapshot

**Snapshot date:** 23 November 2026  
**Source:** Read-only operational aggregation of the deployed system's records.  
**Nature:** Static portfolio evidence, **not** a realtime public telemetry endpoint.

| Metric | Recorded value | Interpretation |
| :-- | --: | :-- |
| Rendered content jobs | **3,091** | Jobs whose stored lifecycle status was `rendered` |
| Published queue records | **837** | Records whose stored publishing status was `published` |
| Published records in prior seven days | **96** | Subset of the published queue, using a trailing seven-day window |
| Indexed X video records | **3,517** | Media-vault entries; includes indexed source videos, not just used or finished videos |
| Registered motion media assets | **403** | Entries in the motion media asset catalog; not a count of published Snapchat videos |

**Important qualifiers**
1. Figures are database-record counts, not independent third-party analytics or social impressions.
2. Multiple records can relate to one event; a rendered graphic may never be approved for publication.
3. Publishing status is a stored operational result. Example post URLs provide spot-checkable public evidence, but this document does not audit every record.
4. There is no defensible labor-hour reduction or ROI figure in this snapshot, so none is claimed.
5. No count of Snapchat auto-publication is claimed.

## Public proof — sampled outputs

- [Match statistic card](https://x.com/TacticSpoort/status/2124629151449583946)
- [Player-of-the-match card](https://x.com/TacticSpoort/status/2124582742360764647)
- [Starting XI graphic](https://x.com/TacticSpoort/status/2124483139678384632)
- [League table](https://x.com/TacticSpoort/status/2124245056773058993)
- [Round analysis](https://x.com/TacticSpoort/status/2124216319578894649)
- [News post](https://x.com/TacticSpoort/status/2124641048093733372)

## Reproducibility and privacy

Detailed event logs, personal identifiers, source payloads, internal traces, system configuration and operational credentials are intentionally omitted. A prospective employer can inspect publicly visible outputs and discuss the architecture at a non-sensitive level.
