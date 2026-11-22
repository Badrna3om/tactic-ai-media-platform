# Engineering Case Study: Multi-Stream Media Operations

## The challenge

Operating a sports-media brand requires continuous intake and triage of events, accurate match and player references, several graphic formats, editorial decisions, human corrections, and channel-specific delivery. A single linear script is brittle for these competing workloads.

## The system-level response

**1. Separate data acquisition from creative production.** Match/event intelligence feeds durable task queues. Newsroom intake uses distinct editorial stages. Media collection has its own lifecycle.

**2. Treat the database as an operational source of truth.** Records track content type, stage, state, retries and final publication/delivery, rather than assuming a successful API call proves the whole operation succeeded.

**3. Preserve human control where it matters.** Editorial operators review, correct, approve or discard items before final publishing.

**4. Design for missing media and duplicates.** Teams, players and media assets must be resolved consistently. The operation contains missing-asset routing and deduplication safeguards.

**5. Support brand-aware outputs.** TACTIC and AMER share production approaches but can use different templates and handoff practices.

**6. Recover, don't silently fail.** The architecture includes lease/retry and recovery patterns, with monitoring of queue progression and unsuccessful tasks.

## Representative trace (published Barcelona–Villarreal items)

| Output stage | Public artifact |
| :-- | :-- |
| Pre-match | [Starting XI card](https://x.com/TacticSpoort/status/2124483139678384632) |
| Match completion | [Statistics card](https://x.com/TacticSpoort/status/2124525366769234248) |
| Individual performance | [Player-of-the-match card](https://x.com/TacticSpoort/status/2124530161156510070) |

This sequence explains a **real content family** from one match, not a perfect one-to-one audit trace for every internal execution.

## Evidence boundary

The numbers in [Production Evidence](PRODUCTION_EVIDENCE.md) are snapshot record counts, not performance SLAs, revenue attribution, time-saved claims, social analytics or independent audit certification.

## Why it transfers

The design patterns apply beyond media:

| TACTIC operation | Comparable business use |
| :-- | :-- |
| Match and news signal | Customer enquiry or CRM lead |
| Relevance classification | Lead intent / document type |
| Data validation | Customer information verification |
| Creative or media generation | Quote, document or report generation |
| Editorial approval | Employee authorization |
| Social publishing | CRM action, customer response, internal handoff |
| Operations log | Audit record and management reporting |

These are **architectural analogies**, not claims that TACTIC already runs these specific non-sports workflows.

## Confidentiality

The private production design is proprietary. This document deliberately excludes exact routing rules, real endpoint addresses, data-provider contracts, full schemas, workflow exports and model prompts.
