<a href="https://github.com/theritikkk">
  <img height=200 align="center" src="https://github-readme-stats.vercel.app/api?username=theritikkk&theme=radical" />
</a>
<a href="https://github.com/theritikkk">
  <img height=200 align="center" src="https://github-readme-stats.vercel.app/api/top-langs?username=theritikkk&layout=compact&langs_count=8&card_width=320&theme=radical" />
</a>
<br><br>

[![trophy](https://github-profile-trophy.vercel.app/?username=theritikkk&theme=radical&title=-Issues)](https://github.com/theritikkk)

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=theritikkk&theme=radical)](https://github.com/theritikkk)



## My Repos

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=theritikkk&repo=AI-ChatBot&theme=radical)](https://github.com/theritikkk/AI-ChatBot) [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=theritikkk&repo=KinoFlow&theme=radical)](https://github.com/tejasnasa/KinoFlow)
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=theritikkk&repo=YelpCamp&theme=radical)](https://github.com/theritikkk/YelpCamp) [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=theritikkk&repo=Login-Page&theme=radical)](https://github.com/tejasnasa/Login-Page)

name: generate animation

on:
  # run automatically every 12 hours
  schedule:
    - cron: "0 */12 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the main branch
  push:
    branches:
    - main
    
  

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v2
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v2.6.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
