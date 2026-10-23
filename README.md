# Hi there, I'm David ⚡

### Cybersecurity Enthusiast & Software Developer

<!-- النص الكتابي المتحرك -->
<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=3000&pause=1000&color=00F0FF&center=true&vCenter=true&width=500&lines=Cybersecurity+%26+Ethical+Hacking;Software+Development+%26+Python;Building+Secure+%26+Scalable+Apps" alt="Typing SVG" />
  </a>
</p>

---

### 💻 Tech Stack & Tools
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,flask,git,github,linux,mysql,bash,docker,postman&theme=dark" />
</p>

---

### 📊 GitHub Profile Stats
<p align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=DavidHany100&show_icons=true&theme=radical&include_all_commits=true&count_private=true" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=DavidHany100&layout=compact&theme=radical&hide=html,css" />
</p>

---

### 📈 Contribution Streak
<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=DavidHany100&theme=radical" alt="GitHub Streak" />
</p>

---

### 🐍 Contribution Snake Animation
name: Generate Snake

on:
  schedule:
    - cron: "0 */12 * * *" 
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
