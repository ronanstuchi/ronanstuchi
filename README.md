
👋 Hi, I’m @ronanstuchi

- 🏘 From São Paulo / Brazil
- 🧐 Front-End
- 🌱 I’m currently learning 
- 👌🙌🎶🎂🐱‍🏍🐱‍🏍🐱‍🐉🎁🐱‍🚀

<div> align="center">
  <a href="https://github.com/ronanstuchi">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=ronanstuchi&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
name: Generate Datas
</div>
  
   name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: ronanstuchi
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
