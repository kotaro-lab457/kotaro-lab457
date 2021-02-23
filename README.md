
<!--
**kotaro-lab457/kotaro-lab457** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="left" src="https://github-readme-stats.vercel.app/api?username=karaage0703&count_private=true&show_icons=true" />
</a>
<a href="https://github.com/anuraghazra/github-readme-stats">
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs/?username=karaage0703" />
</a>

name: GitHub-Profile-Summary-Cards

on:
  schedule: # execute every 24 hours
    - cron: "* */24 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate

    steps:
      - uses: actions/checkout@v2
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env: # default use ${{ secrets.GITHUB_TOKEN }}, you can change to your personal access token
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}
