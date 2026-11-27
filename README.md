# Odoo 18 → 20 Migration Demonstrations

**RAQQA | Synapse Migration MCP**

Evidence-based AI-assisted addon migration demonstrations, not official OCA releases or production-ready upgrades.

## Explore the migration

| Resource | Description |
| --- | --- |
| [Odoo 18 — Original source](https://github.com/raqqa-owener/odoo-migration-18-20/tree/18.0) | Original OCA addon files |
| [Odoo 20 — Migrated candidate](https://github.com/raqqa-owener/odoo-migration-18-20/tree/20.0) | Synapse migration candidate c7 |
| [Compare 18.0 → 20.0](https://github.com/raqqa-owener/odoo-migration-18-20/compare/18.0...20.0) | 12 changed addon files and one migration notice |
| [Visual Migration Report](https://raqqa-owener.github.io/odoo-migration-18-20/g28a-public-report.html) | Screenshots and verification results |
| [Detailed verification summary](demos/multi-company/verification.md) | Recorded evidence and limitations |

## Multi-company foundation (G28-A)

Four interdependent addons from [OCA/multi-company](https://github.com/OCA/multi-company/tree/612aa72f3265d75c6b73bf893b1ffe8aa7f20fe0): `base_multi_company`, `partner_multi_company`, `product_multi_company`, and `product_multi_company_stock`.

### Recorded results — 27 November 2026

| Verification | Result |
| --- | --- |
| Odoo 18 native tests | 42 passed |
| Odoo 20 candidate c7 native tests | 41 passed, 1 error |
| Primary business suite | 14/14 matched |
| Combined business suites | 17 matches, 8 differences, 1 error (26 cases, including an older defective probe) |
| Browser comparisons | 3, review required |
| Manual addon code fixes | 0 during measured sessions 02–04 |
| Delivery status | REVIEW only |

Native test infrastructure and fixtures were adapted for Odoo 20. Claude generated and verified the candidate using Synapse Migration MCP. Codex subsequently retrieved the same evidence through the local MCP; it has not yet performed an independent migration in this case study.

### Approach

Synapse supports structural extraction, business scenario design, source baseline capture, compatibility repair, isolated runtime verification, native and business test comparison, browser validation, and integrated review delivery. Unresolved differences are preserved rather than treated as successful migration outcomes.

### Release status

**Not approved for production deployment.** An unresolved access-control issue and other review gaps remain. Existing database upgrades have not been demonstrated. The pinned standard source commits have not been proven identical to the runtime images. Results are recorded project evidence, not independent certification.

The original and migrated addon source trees are available in the version branches with license texts and a migration modification notice. Full internal evidence is not published. The candidate remains review-only, with an unresolved access-control finding; production deployment and uninstall are not approved. The proprietary Synapse engine, skills and private project knowledge are not distributed here. Original addon authors retain their respective copyright and license notices; no OCA affiliation or endorsement is implied.

## Contact

RAQQA — info@rakka.co.jp

We welcome technical evaluations by Odoo implementation and migration partners.
