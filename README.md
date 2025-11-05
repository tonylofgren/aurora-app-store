# Aurora App Store

Official entry point for Aurora apps using a **decentralized model**.

- Each app lives in its own GitHub repository.
- Every app includes an `aurora-manifest.json` in the repository root.
- App versions are managed via GitHub Releases.
- This repository provides:
  - `default-repos.json` – list of verified apps (approved by you)
  - Developer specification and schema under `docs/`
  - Automated moderation using Issues and Labels

---

## 🔍 How discovery works

Aurora clients can run in three modes:

| Mode | Behavior | Use case |
|------|-----------|-----------|
| **Strict** | Load apps only from `default-repos.json` | Only verified apps |
| **Hybrid** | Load `default-repos.json` + GitHub search for repos with topic `aurora-app` | Show verified + community |
| **Open** | Show all repos with topic `aurora-app` | Full community listing |

---

## 🧩 Moderation flow

1. A developer submits an **Issue** using the app submission form.
2. The validation workflow checks:
   - Repo is public  
   - Contains `aurora-manifest.json`  
   - Has GitHub topic `aurora-app`  
   - Has at least one Release (`vX.Y.Z`)
3. You then label the Issue:
   - 🟢 `submission:approved` → Creates a PR adding the repo to `default-repos.json`
   - 🔴 `submission:remove` → Creates a PR removing the repo

---

## 🏷️ Required Labels
Create these labels in your repo:
- `submission:pending`
- `submission:approved`
- `submission:remove`
- `submission:changes-requested`
- `submission:blocked` (optional)

---

## 🧠 For developers
- Follow the [Manifest Spec](docs/manifest-spec.md)
- Add topic **`aurora-app`** to your repository
- Publish at least one release (`v1.0.0`)
