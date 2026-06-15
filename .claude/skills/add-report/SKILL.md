---
name: add-report
description: Add a security report PDF to the repo — reads the project + audit name from the PDF, copies it into reports/, and adds a numbered entry under the current year in README.md.
---

# Add a security report

The user invokes this and pastes (or references) a report PDF. Do this:

1. **Read the PDF** to extract the title as `<Project Name> - <Audit Name>` (e.g. `LI.FI - Mayan V2.0`). Both come from the cover page.

2. **Copy the PDF into `reports/`.** Match the existing naming style: `YYYY-MM-<Project>-<Audit>.pdf` (use the report date from the cover page). Keep it close to the title; don't overthink it.

3. **Edit `README.md`.** Under the matching `## YYYY` year heading (report's year), append the next numbered list item:
   ```
   N. [<Project Name> - <Audit Name>](./reports/<filename>.pdf)
   ```
   - `N` = continue the existing numbering in that section.
   - If the year section doesn't exist, create it above the previous year (newest year first).

4. Report back the title, filename, and the line added. Don't commit unless asked.

Keep it minimal — no extra files, no extra prose in README.
