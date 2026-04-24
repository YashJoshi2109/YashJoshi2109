# GitHub Profile Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `README.md` into a beautiful, recruiter-friendly GitHub profile with animated headline, condensed bio, social badges, grouped tech stack icons, GitHub stats/streak/languages cards, activity graph, trophies, and contribution snake.

**Architecture:** Single-file rewrite of `README.md` using external badge/stats services (no backend, no auth). All sections built incrementally, assembled in final task. Each task appends one section to a working README.

**Tech Stack:** `readme-typing-svg.demolab.com`, `github-readme-stats.vercel.app`, `streak-stats.demolab.com`, `github-readme-activity-graph.vercel.app`, `github-profile-trophy.vercel.app`, `skillicons.dev`, `img.shields.io`

---

## File Map

| File | Action | Responsibility |
|------|--------|----------------|
| `README.md` | Rewrite | Full profile page |
| `.github/workflows/snake.yml` | Already done | Snake animation generation |

---

### Task 1: Write base README with header + typing animation

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Replace entire README with header section**

Replace full contents of `README.md` with:

```markdown
<div align="center">
  <img src="banner_github.jpg" alt="GitHub Banner" width="100%" />

  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=00D4FF&center=true&vCenter=true&width=600&lines=Data+Scientist;ML+Engineer+%26+AI+Engineer;Open+Source+Builder;MS+%40+UT+Arlington" alt="Typing SVG" />
  </a>
</div>

<br/>
```

- [ ] **Step 2: Verify typing animation URL renders**

Open in browser:
```
https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=00D4FF&center=true&vCenter=true&width=600&lines=Data+Scientist;ML+Engineer+%26+AI+Engineer;Open+Source+Builder;MS+%40+UT+Arlington
```
Expected: animated cyan typing SVG cycling through all 4 phrases.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add profile header with banner and typing animation"
```

---

### Task 2: Add About Me section

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append About Me section**

Append to `README.md`:

```markdown
## 💫 About Me

- 🎓 **MS Data Science** @ University of Texas at Arlington
- 🤝 **Collaborating on:** End-to-end DS solutions, Hackathons, MLOps, AI in education/sustainability/smart cities
- 🌱 **Currently learning:** Advanced data engineering, transformer models, cloud-native AI (AWS/GCP)
- 💬 **Ask me about:** ML pipeline design, LLMs, FastAPI + Docker deployment, hackathon architecture
- 🤗 **AI Builder:** Trained & published multi-modal AI models on HuggingFace spanning NLP, computer vision, and generative AI
- ⚡ **Fun fact:** Built a full CI/CD analytics dashboard (Jenkins + Docker + K8s + GitHub Actions) in a single hackathon weekend

<br/>
```

- [ ] **Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add condensed About Me section"
```

---

### Task 3: Add Socials row with HuggingFace badge

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append Socials section**

Append to `README.md`:

```markdown
## 🌐 Socials

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/yashjoshi2124)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yash-joshi21)
[![X](https://img.shields.io/badge/X-black.svg?style=for-the-badge&logo=X&logoColor=white)](https://x.com/yashjosh7486)
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)](https://youtube.com/@Yash_Joshi)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-%23FFD21E.svg?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/yashj2110)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yashjosh7486@gmail.com)

</div>

<br/>
```

- [ ] **Step 2: Verify HuggingFace badge renders**

Open in browser:
```
https://img.shields.io/badge/HuggingFace-%23FFD21E.svg?style=for-the-badge&logo=huggingface&logoColor=black
```
Expected: yellow HuggingFace badge with logo.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add socials row with HuggingFace badge"
```

---

### Task 4: Add Tech Stack section (grouped skillicons rows)

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append Tech Stack section**

Append to `README.md`:

```markdown
## 🛠️ Tech Stack

<div align="center">

**Languages**

[![Python](https://skillicons.dev/icons?i=py)](https://python.org)
[![R](https://skillicons.dev/icons?i=r)](https://r-project.org)
[![Bash](https://skillicons.dev/icons?i=bash)](https://gnu.org/software/bash)
![SQL](https://img.shields.io/badge/SQL-%2300D4FF.svg?style=flat-square&logo=postgresql&logoColor=white)

**ML / AI**

[![TensorFlow](https://skillicons.dev/icons?i=tensorflow)](https://tensorflow.org)
[![PyTorch](https://skillicons.dev/icons?i=pytorch)](https://pytorch.org)
[![OpenCV](https://skillicons.dev/icons?i=opencv)](https://opencv.org)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-%23150458.svg?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-%23013243.svg?style=flat-square&logo=numpy&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-%23FFD21E.svg?style=flat-square&logo=huggingface&logoColor=black)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%2300D4FF.svg?style=flat-square&logo=python&logoColor=white)

**Data Engineering**

![Apache Spark](https://img.shields.io/badge/Apache%20Spark-%23E25A1C.svg?style=flat-square&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-%23017CEE.svg?style=flat-square&logo=apacheairflow&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-%23231F20.svg?style=flat-square&logo=apachekafka&logoColor=white)

**Databases**

[![PostgreSQL](https://skillicons.dev/icons?i=postgres)](https://postgresql.org)
[![MySQL](https://skillicons.dev/icons?i=mysql)](https://mysql.com)
[![MongoDB](https://skillicons.dev/icons?i=mongodb)](https://mongodb.com)
[![Redis](https://skillicons.dev/icons?i=redis)](https://redis.io)

**Cloud**

[![AWS](https://skillicons.dev/icons?i=aws)](https://aws.amazon.com)
[![GCP](https://skillicons.dev/icons?i=gcp)](https://cloud.google.com)
[![Azure](https://skillicons.dev/icons?i=azure)](https://azure.microsoft.com)

**DevOps / MLOps**

[![Docker](https://skillicons.dev/icons?i=docker)](https://docker.com)
[![Kubernetes](https://skillicons.dev/icons?i=kubernetes)](https://kubernetes.io)
[![Jenkins](https://skillicons.dev/icons?i=jenkins)](https://jenkins.io)
[![GitHub Actions](https://skillicons.dev/icons?i=githubactions)](https://github.com/features/actions)
![MLflow](https://img.shields.io/badge/MLflow-%230194E2.svg?style=flat-square&logo=mlflow&logoColor=white)

**Frameworks & IDEs**

[![FastAPI](https://skillicons.dev/icons?i=fastapi)](https://fastapi.tiangolo.com)
[![Flask](https://skillicons.dev/icons?i=flask)](https://flask.palletsprojects.com)
[![VS Code](https://skillicons.dev/icons?i=vscode)](https://code.visualstudio.com)
[![Jupyter](https://skillicons.dev/icons?i=jupyter)](https://jupyter.org)
![Streamlit](https://img.shields.io/badge/Streamlit-%23FF4B4B.svg?style=flat-square&logo=streamlit&logoColor=white)

</div>

<br/>
```

- [ ] **Step 2: Verify skillicons batch URL renders**

Open in browser:
```
https://skillicons.dev/icons?i=py,r,bash,tensorflow,pytorch,opencv,postgres,mysql,mongodb,redis,aws,gcp,azure,docker,kubernetes,jenkins,githubactions,fastapi,flask,vscode,jupyter
```
Expected: grid of colored tech icons.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add grouped tech stack section with skillicons and shields badges"
```

---

### Task 5: Add GitHub Stats + Streak cards side by side

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append stats section**

Append to `README.md`:

```markdown
## 📊 GitHub Stats

<div align="center">

<table>
  <tr>
    <td>
      <img src="https://github-readme-stats.vercel.app/api?username=YashJoshi2109&show_icons=true&bg_color=0d1117&title_color=00D4FF&text_color=ffffff&icon_color=00D4FF&border_color=00D4FF&count_private=true&hide_border=false" alt="GitHub Stats" />
    </td>
    <td>
      <img src="https://streak-stats.demolab.com?user=YashJoshi2109&background=0d1117&ring=00D4FF&fire=00D4FF&currStreakLabel=00D4FF&sideLabels=ffffff&dates=888888&border=00D4FF&stroke=00D4FF" alt="GitHub Streak" />
    </td>
  </tr>
</table>

</div>

<br/>
```

- [ ] **Step 2: Verify stats card URL renders**

Open in browser:
```
https://github-readme-stats.vercel.app/api?username=YashJoshi2109&show_icons=true&bg_color=0d1117&title_color=00D4FF&text_color=ffffff&icon_color=00D4FF&border_color=00D4FF&count_private=true
```
Expected: dark card with cyan accents showing stars, commits, PRs.

- [ ] **Step 3: Verify streak card URL renders**

Open in browser:
```
https://streak-stats.demolab.com?user=YashJoshi2109&background=0d1117&ring=00D4FF&fire=00D4FF&currStreakLabel=00D4FF&border=00D4FF
```
Expected: dark streak card with cyan ring and fire icons.

- [ ] **Step 4: Commit**

```bash
git add README.md
git commit -m "feat: add GitHub stats and streak cards side by side"
```

---

### Task 6: Add Top Languages card

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append Top Languages card**

Append to `README.md`:

```markdown
<div align="center">

  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YashJoshi2109&layout=compact&bg_color=0d1117&title_color=00D4FF&text_color=ffffff&border_color=00D4FF&hide_border=false&langs_count=10" alt="Top Languages" />

</div>

<br/>
```

- [ ] **Step 2: Verify top languages URL renders**

Open in browser:
```
https://github-readme-stats.vercel.app/api/top-langs/?username=YashJoshi2109&layout=compact&bg_color=0d1117&title_color=00D4FF&text_color=ffffff&border_color=00D4FF&langs_count=10
```
Expected: compact dark card showing top languages with cyan title.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add top languages card"
```

---

### Task 7: Add Activity Graph

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append activity graph section**

Append to `README.md`:

```markdown
## 📈 Activity Graph

<div align="center">

  <img src="https://github-readme-activity-graph.vercel.app/graph?username=YashJoshi2109&bg_color=0d1117&color=00D4FF&line=00D4FF&point=ffffff&area=true&area_color=00D4FF&hide_border=false&border_color=00D4FF" alt="Contribution Graph" width="100%" />

</div>

<br/>
```

- [ ] **Step 2: Verify activity graph URL renders**

Open in browser:
```
https://github-readme-activity-graph.vercel.app/graph?username=YashJoshi2109&bg_color=0d1117&color=00D4FF&line=00D4FF&point=ffffff&area=true&border_color=00D4FF
```
Expected: full-width dark graph with cyan line and area fill showing contribution history.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add full-width activity graph"
```

---

### Task 8: Add GitHub Trophies

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append trophies section**

Append to `README.md`:

```markdown
## 🏆 Trophies

<div align="center">

  <img src="https://github-profile-trophy.vercel.app/?username=YashJoshi2109&theme=darkhub&no-frame=true&no-bg=true&margin-w=4&column=7" alt="GitHub Trophies" />

</div>

<br/>
```

- [ ] **Step 2: Verify trophies URL renders**

Open in browser:
```
https://github-profile-trophy.vercel.app/?username=YashJoshi2109&theme=darkhub&no-frame=true&no-bg=true&margin-w=4&column=7
```
Expected: row of dark-themed trophies (commits, PRs, repos, stars, etc.)

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add GitHub trophies row"
```

---

### Task 9: Add Contribution Snake + final dividers

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append snake section**

Append to `README.md`:

```markdown
## 🐍 Contribution Snake

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/YashJoshi2109/YashJoshi2109/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/YashJoshi2109/YashJoshi2109/output/github-snake.svg" />
  <img alt="github contribution snake" src="https://raw.githubusercontent.com/YashJoshi2109/YashJoshi2109/output/github-snake.svg" />
</picture>

</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=YashJoshi2109&color=00D4FF&style=flat-square&label=Profile+Views" alt="Profile Views" />
</div>
```

Note: Profile view counter uses `komarev.com/ghpvc` — free, no auth needed, auto-increments on each profile visit.

- [ ] **Step 2: Verify profile view counter renders**

Open in browser:
```
https://komarev.com/ghpvc/?username=YashJoshi2109&color=00D4FF&style=flat-square&label=Profile+Views
```
Expected: cyan flat badge showing view count.

- [ ] **Step 3: Remove old snake embed duplicate (if present)**

Check `README.md` for any duplicate snake section from the earlier fix. If the `## 🐍 Contribution Graph` block exists from the previous session, remove it — only one snake section should exist (this one, under `## 🐍 Contribution Snake`).

- [ ] **Step 4: Final commit**

```bash
git add README.md
git commit -m "feat: add contribution snake and profile view counter — complete profile redesign"
```

---

## Verification Checklist

After all tasks complete and pushed to GitHub:

- [ ] Visit `github.com/YashJoshi2109` — typing animation cycles all 4 phrases
- [ ] About Me bullets readable in under 10 seconds
- [ ] All 6 social badges link correctly (Discord, LinkedIn, X, YouTube, HuggingFace, Email)
- [ ] All tech stack icons render (no broken images)
- [ ] Stats card shows real numbers (not zeros)
- [ ] Streak card shows contribution ring
- [ ] Top languages card shows actual languages
- [ ] Activity graph shows contribution history line
- [ ] Trophies row renders at least 4 trophies
- [ ] Snake animation visible (after manually triggering the GitHub Action once)
- [ ] Profile view counter increments on refresh
- [ ] Dark mode: snake switches to dark SVG, all cards stay dark-themed
