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
**Issue Reproduction Confirmed:** I ran the ingestion pipeline locally and input a test document containing the words "JavaScript" and "TypeScript". The resulting parsed output failed to extract either language as a skill, confirming the bug exists in my local environment.