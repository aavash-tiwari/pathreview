## Week 7 Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/148
**Issue title:** Skill extractor fails to detect JavaScript and TypeScript
**Tier:** [X] Tier 1 [ ] Tier 2 [ ] Tier 3

**Problem summary:**
This issue occurs in the backend ingestion pipeline where the system scans documents for technical skills. Currently, the extractor fails to recognize 'JavaScript' and 'TypeScript' as valid skills when parsing text, likely due to a missing keyword mapping or regex oversight. A successful fix will update the skill detection logic to correctly identify and extract these two languages so they appear accurately in the parsed output. I selected this Tier 1 issue because its scope is strictly limited to the ingestion pipeline's text parsing logic; updating a skill detection list is a highly isolated backend task that matches my current comfort level, making it a perfectly scoped entry point into this large codebase.

**Branch name:** fix/148-skill-extractor-js-ts
**Setup confirmation:** (X) App runs locally at localhost:5173
**Cohort ledger:** (X) Issue added to cohort ledger

**Selection Notes ("Is this right for me?" Checklist):**
* **Is it actually open?** Yes, the issue is currently open. While there are 2 linked PRs, the project guidelines state claims are not exclusive, so I can review those PRs to see what approaches might have failed or what my peers are doing.
* **Is the scope clear?** Yes, it clearly specifies the exact two languages (JavaScript and TypeScript) that are failing to extract.
* **Is it the right size?** Yes, as a Tier 1 issue, it is highly isolated to just the ingestion module.
* **Is the maintainer active?** Yes, the issue was recently opened by a maintainer and the thread is active.
* **Does it match where you are?** Yes, string matching and keyword extraction in Python aligns perfectly with my current development skills.

## Week 8 Reproduction & solution planning

**Reproduction commit link:** https://github.com/aavash-tiwari/pathreview/commits/fix/148-skill-extractor-js-ts
**Reproduction summary:**
I successfully reproduced the issue by tracing the ingestion pipeline's behavior. When processing a test string containing "JavaScript" and "TypeScript", the extractor dropped both languages, confirming the keyword mapping is missing locally.

**PLAN.md link:** https://github.com/aavash-tiwari/pathreview/blob/fix/148-skill-extractor-js-ts/PLAN.md
**Walkthrough video (recommended):** N/A
**Blockers or open questions:**
None at this time. The scope is well-defined and isolated to the ingestion module.