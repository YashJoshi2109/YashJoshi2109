# GitHub Profile Redesign — Design Spec
**Date:** 2026-04-24
**Author:** Yash Joshi

---

## Overview

Full redesign of `YashJoshi2109/YashJoshi2109` GitHub profile README. Goal: aesthetic, recruiter-friendly profile with real GitHub stats, charts, tech stack visualization, and animated contribution graph.

---

## Theme

| Property | Value |
|----------|-------|
| Background | Dark (`#0d1117` — GitHub dark default) |
| Accent | Cyan `#00D4FF` |
| Text | White / light gray |
| Font style | Monospace where possible |
| Tone | Clean, minimal, data-science identity |

---

## Layout — Narrative First (Layout B)

Recruiter reads top-to-bottom. Story → identity → proof (stats).

```
banner_github.jpg (full width)
Typing animation headline
────────────────────────────
About Me (condensed bullets)
────────────────────────────
Socials row
────────────────────────────
Tech Stack (grouped by category)
────────────────────────────
GitHub Stats (side by side: Stats card | Streak card)
Top Languages card
────────────────────────────
Activity Graph (full width)
────────────────────────────
GitHub Trophies row
────────────────────────────
Contribution Snake (dark/light auto-switch)
```

---

## Section Specs

### 1. Header

- Image: `banner_github.jpg` at 100% width
- Animated typing SVG via `readme-typing-svg.demolab.com`
  - Cycles: `"Data Scientist"` → `"ML Engineer"` → `"Open Source Builder"` → `"MS @ UT Arlington"`
  - Color: `#00D4FF`, font: monospace, size: 22px, center-aligned

### 2. About Me

Rewritten as tight bullet points (not wall of text):
- Currently: MS Data Science @ UT Arlington
- Collaborating on: end-to-end DS solutions, MLOps, AI in education/sustainability/smart cities
- Learning: advanced data engineering, transformer models, cloud-native AI (AWS/GCP)
- Ask me about: ML pipeline design, FastAPI + Docker deployment, hackathon architecture
- Fun fact: built full CI/CD analytics dashboard (Jenkins + Docker + K8s + GitHub Actions) in a single hackathon weekend

### 3. Socials

Shields.io badges, horizontal row:

| Platform | Link |
|----------|------|
| Discord | `https://discord.gg/yashjoshi2124` |
| LinkedIn | `https://www.linkedin.com/in/yash-joshi21` |
| X (Twitter) | `https://x.com/yashjosh7486` |
| YouTube | `https://youtube.com/@Yash_Joshi` |
| HuggingFace | `https://huggingface.co/yashj2110` |
| Email | `yashjosh7486@gmail.com` |

### 4. Tech Stack

Uses `skillicons.dev` icon rows, grouped by category:

| Category | Tools |
|----------|-------|
| Languages | Python, SQL, Bash, R |
| ML / AI | TensorFlow, PyTorch, scikit-learn, Pandas, NumPy, Matplotlib, Hugging Face, OpenCV |
| Data Engineering | Apache Spark, Airflow, Kafka |
| Databases | PostgreSQL, MySQL, MongoDB, Redis |
| Cloud | AWS, GCP, Azure |
| DevOps / MLOps | Docker, Kubernetes, Jenkins, GitHub Actions, MLflow |
| Frameworks & IDEs | FastAPI, Flask, Streamlit, VS Code, Jupyter |

### 5. GitHub Stats

Two cards side by side using HTML table:
- Left: `github-readme-stats` — stars, commits, PRs, issues, dark theme, cyan title color
- Right: `streak-stats.demolab.com` — current streak, longest streak, total contributions, dark theme, cyan ring

Below: Top Languages card — compact layout, dark theme, cyan text

All cards: `bg_color=0d1117`, `title_color=00D4FF`, `text_color=ffffff`, `border_color=00D4FF`

### 6. Activity Graph

- Service: `github-readme-activity-graph.vercel.app`
- Full width
- Theme: `react-dark` or custom with `bg_color=0d1117&color=00D4FF&line=00D4FF&point=ffffff`

### 7. GitHub Trophies

- Service: `github-profile-trophy.vercel.app`
- Theme: `darkhub` or `onedark`
- Full row, no-frame, dark background

### 8. Contribution Snake

Already implemented. Auto dark/light switch via `<picture>` tag.
- Dark: `github-snake-dark.svg`
- Light: `github-snake.svg`
- Source: `output` branch, deployed by `.github/workflows/snake.yml`

---

## External Services

| Service | Purpose |
|---------|---------|
| `readme-typing-svg.demolab.com` | Animated typing headline |
| `github-readme-stats.vercel.app` | Stats card + Top Languages |
| `streak-stats.demolab.com` | Streak card |
| `github-readme-activity-graph.vercel.app` | Activity graph |
| `github-profile-trophy.vercel.app` | Trophies |
| `skillicons.dev` | Tech stack icons |
| `img.shields.io` | Social badges |

All services are free, no auth required, no API keys needed.

---

## Files Changed

| File | Change |
|------|--------|
| `README.md` | Full rewrite |
| `.github/workflows/snake.yml` | Already moved (done) |

---

## Success Criteria

- Profile loads with no broken images
- Stats cards show real GitHub data
- Dark/light snake switches correctly
- Tech stack icons render all tools
- Typing animation cycles all 4 phrases
- Recruiter can scan key info in under 10 seconds
