# 🛰️ SpaceDMV Bug Triage Workflow
A standardized process for evaluating, prioritizing, and resolving bugs across the SpaceDMV system.

This workflow ensures stability, transparency, and civilian‑safe operation across all modules, including:
- Authentication
- SVIN/EVIN Registration
- Appointment Scheduling
- UI/UX Framework
- Layout & Navigation

---

## 1. 🚨 Bug Intake

### Sources of incoming bugs:
- GitHub Issues (Bug Report Template)
- Internal testing
- Community feedback
- Security disclosures (handled separately via SECURITY.md)

### Required information:
- Clear reproduction steps
- Expected vs. actual behavior
- Screenshots or recordings
- Affected module(s)
- Environment details

Issues missing critical information are labeled:
**`needs-info`**

---

## 2. 🧭 Initial Classification

A maintainer reviews the report and assigns:

### **Type**
- `bug`
- `regression`
- `ui-bug`
- `performance`
- `accessibility`
- `security` (redirected to private channel)

### **Module**
- `auth`
- `svin`
- `evin`
- `appointments`
- `ui-framework`
- `layout`
- `docs`

### **Status**
- `triage`
- `investigating`
- `confirmed`
- `blocked`
- `in-progress`
- `ready-for-review`
- `resolved`

---

## 3. 🎯 Severity Assessment

Maintainers assign a severity level:

### **🟥 Critical**
- Breaks core workflows (Auth, SVIN/EVIN, Scheduling)
- Security vulnerabilities
- Data corruption
- Complete UI failure

Requires **immediate action**.

### **🟧 High**
- Major feature broken
- Incorrect calculations or logic
- Severe UI/UX degradation

### **🟨 Medium**
- Non‑blocking bugs
- Minor UI issues
- Workflow inconsistencies

### **🟩 Low**
- Cosmetic issues
- Typos
- Minor layout misalignment

---

## 4. 🗂️ Priority Assignment

Severity determines priority, but maintainers may adjust based on:

- Impact on civilians
- Impact on examiners/officers
- Release timelines
- Security implications
- Architectural risk

### Priority Levels:
- `P0` — Immediate fix (Critical)
- `P1` — High priority (High)
- `P2` — Standard priority (Medium)
- `P3` — Low priority (Low)

---

## 5. 🔍 Reproduction & Confirmation

A maintainer or contributor attempts to reproduce the bug.

If reproducible:
- Issue is marked **`confirmed`**
- Assigned to a module owner

If not reproducible:
- Marked **`cannot-reproduce`**
- Reporter is asked for more details

---

## 6. 🧪 Assignment & Investigation

The issue is assigned to:
- A module owner  
or  
- A contributor who volunteers

Assignee updates the issue with:
- Findings
- Logs
- Screenshots
- Hypotheses

If blocked by another issue:
- Add label **`blocked`**
- Link the dependency

---

## 7. 🛠️ Fix Development

Fixes must:
- Follow coding standards
- Include tests (if applicable)
- Update documentation (if needed)
- Include screenshots for UI changes

A pull request is opened with:
- Clear description
- Linked issue
- Before/after visuals

---

## 8. 🔄 Review & Approval

### Review Requirements:
- **Minor fixes:** 1 maintainer approval  
- **Major fixes:** 2 maintainer approvals  
- **Security fixes:** Maintainer‑only, private review  

Reviewers check:
- Code quality
- Architecture alignment
- Regression risk
- UI/UX consistency
- Documentation updates

---

## 9. 🚀 Merge & Deployment

Once approved:
- PR is merged into `dev`
- Automated checks run
- Included in next release cycle

Critical fixes may be hot‑patched into `main`.

---

## 10. 📦 Post‑Resolution

After merging:
- Issue is marked **`resolved`**
- Linked PR is referenced
- Release notes are updated
- Documentation is updated (if needed)

If the bug reappears:
- A new issue is opened
- Marked as **`regression`**

---

## 11. 📊 Metrics & Reporting

Maintainers track:
- Time to triage
- Time to resolution
- Number of regressions
- Module‑specific bug density
- Severity distribution

These metrics inform:
- Roadmap updates
- Architecture improvements
- Module ownership adjustments

---

## 12. 🛡️ Security‑Related Bugs

Security bugs follow the process in:
**SECURITY.md**  
and are **never** handled publicly.

---

## 13. 🙏 Acknowledgment

This workflow is inspired by industry‑standard triage systems and adapted for the mission, ethics, and structure of the LEAF Universe.

Thank you for helping keep SpaceDMV stable, safe, and civilian‑friendly.

