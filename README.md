# Interface Critique & Research Question Canvas

**Case:** Online scholarship application (education / public-service workflow)
**Author:** Shamili, B.E. Computer Science and Engineering, Sri Krishna College of Engineering and Technology, Coimbatore

## Links
- **Figma critique board:** (add your Figma link here)

## Overview
Many education and public-service portals confuse users with unclear labels, hidden rules, cryptic errors and vague status messages. This project critiques one such workflow, an online scholarship application, and defines a defensible design problem **before any redesign screens are drawn**.

> The screens in `images/` are recreated illustrations with dummy content. The evidence comes from a heuristic review, and no participants have been interviewed yet, so confidence is marked Low until it is tested with real users.

## Journey (5 annotated screens)
![Journey overview](images/journey-overview.png)

| Screen | Key issue |
|---|---|
| S1 Landing | Unlabeled entry paths, jargon |
| S2 Registration | Hidden password rules, generic error, hard CAPTCHA |
| S3 Profile form | Long form, placeholder-only labels, no autosave |
| S4 Document upload | "Error 1023", limits not shown, low contrast |
| S5 Status | "Pending at Level 1", no timeline or help |

## Research question
**What causes first-time scholarship applicants to fail or abandon each step of the online application, and which interface changes would let them complete it and trust the result without outside help?**

## Assumptions to validate
1. Applicants fail mainly because document requirements and formats are unclear before they start.
2. Inline errors, progress and autosave will cut failed or abandoned submissions.
3. Plain-language status plus a timeline will reduce helpdesk dependence and raise trust.

## Heuristic review
Findings are rated 1 to 4 for severity across clarity, feedback, error prevention, accessibility and trust. There are 13 findings in total, and the critical ones are the CAPTCHA with no alternative, no autosave, the cryptic upload error, and the missing receipt or help contact. See `docs/heuristic-review.md`.

## Deliverables
| Item | Location |
|---|---|
| Annotated screens | `images/` |
| One-page research question canvas | `docs/research-question-canvas.md` |
| Heuristic review | `docs/heuristic-review.md`, `data/heuristic_findings.csv` |
| Evidence log | `data/evidence.csv` |
| Figma workspace setup (Evidence, Research, Flows, UI, Prototype) | `docs/figma-workspace-setup.md` |
| Database | `database/critique.db`, `database/schema.sql` |
| Source code | `src/` |

## Run locally
```bash
pip install pillow
python src/generate_images.py   # regenerate annotated screens
python src/build_db.py          # regenerate CSVs and the SQLite database
sqlite3 database/critique.db < src/queries.sql
```

## Next steps
- Replace the illustrated screens with real anonymised screenshots.
- Run task-based usability tests with 5 or more participants and add consented quotes to the evidence log.
- Validate the three assumptions, then begin redesign in the Figma UI and Prototype pages.

## Privacy
No personal data is stored. Interview quotes, when added, must be consented, non-sensitive and anonymised.
