## 1 · Open-Source Release Checklist 🗒️

| #                               | Task                                                                    | How to Verify                             | Owner      | Status |
| ------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------- | ---------- | ------ |
| **Licensing & IP**              |                                                                         |                                           |            |        |
| 1                               | Select license (Apache-2.0, MIT, etc.) and add `LICENSE` file           | File present at repo root                 | Legal      | ✅      |
| 2                               | Confirm third-party code/data are compatible with chosen license        | Legal sign-off e-mail                     | Legal      | ✅      |
| **Privacy & Data Sanitisation** |                                                                         |                                           |            |        |
| 3                               | Run **PrivacyGuard** batch job on all sample datasets / model artefacts | PrivacyGuard report shows “0 PII found”   | Data Eng   | ❌      |
| 4                               | Delete or mask any residual proprietary identifiers (CUSIP lists etc.)  | Manual diff check against raw source      | Data Eng   | ❌      |
| **Security Hardening**          |                                                                         |                                           |            |        |
| 5                               | Remove secrets / keys from code & `.env.example`                        | Automated git-secrets scan passes         | DevOps     | ✅      |
| 6                               | Run Static Application Security Test (SAST) on code                     | SAST pipeline green                       | DevOps     | ✅      |
| **Code Quality & Docs**         |                                                                         |                                           |            |        |
| 7                               | Add `README.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`                | Files render correctly on GitHub          | Maintainer | ✅     |
| 8                               | Generate Model Card(s) (`model_card.md`) for each exported model        | Card includes data, metrics, limitations  | ML Lead    | ✅      |
| **Community Readiness**         |                                                                         |                                           |            |        |
| 9                               | Create issue & PR templates                                             | Templates appear in “New Issue” UI        | Maintainer | ✅      |
| **Release Logistics**           |                                                                         |                                           |            |        |
| 10                              | Publish Hugging Face model(s) with matching tag & README                | HF repo reflects same license & version   | ML Lead    | ✅      |
| 11                              | Announce release on internal comms + public channels (optional)         | Post in Slack / LinkedIn / mailing list   | Comms      | ✅      |
