# Contributing Guide

Thank you for considering a contribution to **Exception‑handling‑reconciliation**!
Your help drives better automation, safer data, and smoother settlements for
capital‑markets operations.

---

## 🛠️ How to Contribute

1. **Fork the repo** and create your feature branch

   ```bash
   git checkout -b feat/my‑awesome‑feature
   ```
2. **Write code + tests**

   * Follow the coding standards below.
   * Add unit tests in `tests/` and run `pytest` locally.
3. **Commit smartly**

   ```bash
   git commit -m "feat(ui): add severity heat‑map colour legend"
   ```

   *Use the Conventional Commits style: `type(scope): subject`.*
4. **Run the linter & pre‑commit hooks**

   ```bash
   pre‑commit run --all‑files
   ```
5. **Push & open a Pull Request (PR)**

   ```bash
   git push origin feat/my‑awesome‑feature
   ```

   Then open a PR against `main`.
6. **Fill out the PR template** & sign the CLA.
7. **Wait for CI** & address any review comments.

---

## 🧪 Test & Build Matrix

| Check                | Tool / Cmd              | CI Stage |
| -------------------- | ----------------------- | -------- |
| Unit tests           | `pytest`                | ✔ tests  |
| Type checking        | `mypy`                  | ✔ tests  |
| Lint / formatting    | `ruff`, `black --check` | ✔ lint   |
| Docker build & smoke | `docker compose build`  | ✔ build  |
| Docs build           | `mkdocs build`          | ✔ docs   |

All checks must pass before a PR is merged.

---

## 📐 Coding Standards

* **Python 3.11+**
* Use **type hints** and run `mypy`.
* `black` formatting, `ruff` for linting.
* Keep functions <60 LOC; favour composition over inheritance.
* Write docstrings in the Google style.

---

## 🔐 Data Privacy

Any new sample datasets or notebooks **must** be processed with
**PrivacyGuard** prior to commit.
[PrivacyGuard](https://privacyguard.vercel.app/)
Run:

```bash
privacyguard anonymize data/raw/my_file.csv --out data/public/
```

Attach the generated `anonymization_report.json` in the PR description.

---

## 📝 Commit Message Style

| Type     | Purpose                                 |
| -------- | --------------------------------------- |
| **feat** | New feature                             |
| **fix**  | Bug fix                                 |
| **docs** | Documentation only                      |
| **test** | Adding or updating tests                |
| **ref**  | Code refactor (no functionality change) |
| **ci**   | CI / build system                       |

Example: `feat(model): add LightGBM quantile inference`

---

## 🌍 Branch Naming

* `feat/<short‑slug>` – new features
* `fix/<short‑slug>` – bug fixes
* `ref/<short‑slug>` – refactors/cleanup
* `docs/<short‑slug>` – documentation updates

---

## 📜 License & CLA

By contributing you agree that your contributions will be licensed under the
MIT License and you sign the **Contributor License Agreement (CLA)** found in
`.github/CLA.md`.

---

## 🙋‍♀️ Need help?

Open an issue with the **Question** label or ping
[@kelvi23](https://github.com/kelvi23) on GitHub Discussions.
