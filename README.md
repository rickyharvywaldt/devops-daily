# DevOps Daily Feed 🌱

This repo automatically collects **daily DevOps data** and keeps my GitHub contribution graph active with natural-looking commits.

The logs are written by a GitHub Actions workflow that runs every 6 hours and makes a random number of commits (0–3 each run).  
That way the contribution graph looks organic while the data itself is useful.

---

## 📂 Logs

### ☸️ Kubernetes
- Folder: [`logs/k8s/`](logs/k8s)
- Example file: `2025-08-23.txt`
- Contains the latest stable Kubernetes release.

### 🔐 CVEs
- Folder: [`logs/cves/`](logs/cves)
- Example file: `2025-08-23.json`
- Contains the 5 most recent CVEs from [cve.circl.lu](https://cve.circl.lu).

### 🐳 Docker
- Folder: [`logs/docker/`](logs/docker)
- Example file: `2025-08-23.txt`
- Contains the latest DockerHub `nginx` tag.

---

## 🔄 How It Works
- Runs every 6 hours (`cron` schedule in GitHub Actions).  
- Each run:
  - Randomly decides whether to log Kubernetes, CVEs, or Docker info.  
  - Writes the result into a **daily file** inside the respective folder.  
  - Commits and pushes changes back to this repo.  

Over time this builds a history of daily DevOps snapshots.

