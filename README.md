<!-- README.md for jas3265 -->

<h1 align="center">Hi, I'm Jasper 👋</h1>

<p align="center">
  <em>aspiring DevOps engineer | cloud enthusiast | open to remote work</em>
</p>

---

### 🚀 Currently Learning

<p align="left">
  <img src="https://img.shields.io/badge/Linux-Ubuntu%20%7C%20Bash-informational?style=flat-square&logo=linux&logoColor=white&color=E95420" alt="Linux">
  <img src="https://img.shields.io/badge/Networking-DNS%20%7C%20TCP/IP-informational?style=flat-square&color=blue" alt="Networking">
  <img src="https://img.shields.io/badge/Git-%20Version%20Control-informational?style=flat-square&logo=git&logoColor=white&color=F05032" alt="Git">
</p>

---

### 🛠 Toolbelt

<p align="left">
  <img src="https://img.shields.io/badge/macOS-M1-informational?style=flat-square&logo=apple&logoColor=white&color=000000" alt="macOS">
  <img src="https://img.shields.io/badge/Terminal-zsh-informational?style=flat-square&color=black" alt="ZSH">
  <img src="https://img.shields.io/badge/Editor-VSCode-informational?style=flat-square&logo=visualstudiocode&logoColor=white&color=007ACC" alt="VSCode">
</p>

---

### 📊 Stats & Updates

<p align="left">
  <img src="https://komarev.com/ghpvc/?username=jas3265&label=Profile%20Views&color=0e75b6&style=flat-square" alt="Profile Views">
</p>

<p align="left">
  <img src="https://img.shields.io/badge/DevOps%20Track-Active-informational?style=flat-square&color=brightgreen" alt="DevOps Track">
  <img src="https://img.shields.io/badge/README%20Last%20Updated-auto--updated-lightgrey?style=flat-square" alt="Last Updated">
</p>

---

### 📁 Projects Coming Soon

<ul>
  <li>Bash scripting exercises</li>
  <li>GitHub Action-based automation</li>
  <li>DevOps portfolio projects</li>
</ul>

---

> 🚧 <em>This profile README updates automatically. Stay tuned as I build my DevOps journey from the ground up.</em>

---

<details>
<summary>📂 Folder/File Structure (for GitHub organization)</summary>

```
jas3265/           # your GitHub profile repo
├── README.md      # the main profile content
└── .github
    └── workflows
        └── update-readme.yml   # GitHub Action (auto-update logic)
```

</details>

---

<details>
<summary>🛠 Auto-update Workflow File (YAML)</summary>

```yaml
name: "🛠 Auto Update README"

on:
  schedule:
    - cron: '0 12 * * 1'  # every Monday at 12:00 UTC
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Update timestamp in README
        run: |
          today=$(date -u '+%Y-%m-%d')
          sed -i "s|README%20Last%20Updated-[^?]*|README%20Last%20Updated-$today|" README.md

      - name: Commit and push if changed
        run: |
          git config --global user.name 'github-actions'
          git config --global user.email 'github-actions@github.com'
          git add README.md
          git diff --cached --quiet || git commit -m "🔄 Auto-update README timestamp"
          git push
```

</details>
