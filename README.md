<div align="center">

<h1>Mishkat Mahabub</h1>
<p>Full Stack Developer · Backend Engineer</p>

<a href="mailto:mahabubmishkat22@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white"/></a>
<a href="https://github.com/MishkatMukit"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github"/></a>

</div>

<br/>

## Tech Stack

<p>
<img src="https://skillicons.dev/icons?i=js,ts,c,cpp"/>
<img src="https://skillicons.dev/icons?i=react,tailwind,bootstrap,html,css"/>
</p>
<p>
<img src="https://skillicons.dev/icons?i=nodejs,express"/>
<img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma"/>
<img src="https://img.shields.io/badge/JWT-black?style=flat-square&logo=jsonwebtokens"/>
</p>
<p>
<img src="https://skillicons.dev/icons?i=postgres,mongodb,mysql"/>
</p>
<p>
<img src="https://skillicons.dev/icons?i=git,github,vscode,postman,firebase,vercel,netlify"/>
</p>

<br/>

## GitHub Stats

<div align="center">
<img height="165" src="https://github-readme-stats.vercel.app/api?username=MishkatMukit&show_icons=true&theme=tokyonight&hide_border=true"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MishkatMukit&layout=compact&theme=tokyonight&hide_border=true"/>
</div>

<br/>

## Contribution Graph

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MishkatMukit/MishkatMukit/output/dist/tetris-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MishkatMukit/MishkatMukit/output/dist/tetris-graph.svg">
  <img alt="Tetris animation on contribution graph" src="https://raw.githubusercontent.com/MishkatMukit/MishkatMukit/output/dist/tetris-graph.svg" width="100%"/>
</picture>

</div>

<sub>Requires a one-time GitHub Actions setup — see below.</sub>

<br/>

---

<details>
<summary><b>Enable the Tetris contribution graph</b></summary>
<br/>

Add this as `.github/workflows/tetris-graph.yml` in your `MishkatMukit/MishkatMukit` repo:

```yaml
name: Generate Tetris Contribution Graph

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches: [main]

jobs:
  generate:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: actions/checkout@v4

      - uses: leereilly/contribution-graph-art@v1
        with:
          github_user_name: ${{ github.repository_owner }}
          output_path: dist/tetris-graph.svg

      - uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Push to `main` and let it run once — the graph above will start rendering automatically.

</details>
