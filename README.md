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
  
