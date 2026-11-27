# Multi-company migration — verification summary

Date: 2026-11-27. Candidate: c7. Status: REVIEW only; production deployment not approved.

## Scope and provenance

Upstream: [OCA/multi-company, 18.0 snapshot](https://github.com/OCA/multi-company/tree/612aa72f3265d75c6b73bf893b1ffe8aa7f20fe0).

| Addon | Source version | Target version | License |
|---|---|---|---|
| base_multi_company | 18.0.1.1.1 | 20.0.1.0.0 | LGPL-3 |
| partner_multi_company | 18.0.1.0.3 | 20.0.1.0.0 | AGPL-3 |
| product_multi_company | 18.0.1.0.1 | 20.0.1.0.0 | AGPL-3 |
| product_multi_company_stock | 18.0.1.0.1 | 20.0.1.0.0 | AGPL-3 |

Both packages contain 102 files. SHA-256 of the reviewed original packages (not downloadable here yet):

- Source: `565a19145e7ff8ffb2043087fa6f36f5d76d960d26337c72dfa0544f94dd28dd`
- Target: `f1a0840ef010fef022a1fbf71757e00a860c7a348c11dbf200471f856545a87f`

## Recorded runtime results

| Suite | Match/pass | Difference/error |
|---|---:|---|
| Source native tests | 42 | 0 |
| Target native tests | 41 | 1 error |
| Primary business suite v2 | 14 | 0 |
| Boundary suite v3 (historical probe retained) | 1 | 4 differences, 1 error |
| Access suite v6 | 2 | 4 differences |
| Combined business suites | 17 | 8 differences, 1 error |

Three browser comparisons (company switching, partner form, product form) require review. Native test infrastructure and fixtures were adapted; the source tests were retained. The 41 target passes are not evidence of complete equivalence. No manual addon code fixes were recorded during sessions 02–04; environment interventions occurred before the final session. The final measurement excluded subsequent report generation, delivery and cleanup. Token usage was unavailable.

## Review boundaries

An unresolved access-control finding blocks production approval. Detailed reproduction information is withheld pending coordinated review. Other unresolved differences and a source-side probe assertion error remain. A stricter target permission behavior was retained rather than bypassed. No existing database upgrade was demonstrated. The pinned standard source commits have not been proven identical to runtime images.

## Evidence integrity

The internal final integrated report and review delivery were generated; the delivery was verified EXACT_MATCH. The project-private knowledge graph was read back with EXACT_READBACK (396 nodes, 651 relationships). These are project-recorded results, not independent certification. The uploaded source and target package hashes and manifest metadata were separately checked when preparing this public summary. The runtime tests were not rerun for publication.

Claude performed migration and verification; Codex later retrieved the same evidence through the MCP. This demonstrates shared evidence access, not a second independent migration.

Original authors retain their copyright and license notices. No affiliation with or endorsement by OCA is implied. Code publication is pending license and security review.
