###  Hello! I'm Matheus


- 🔭 Passionate about technology
- 🌱 Student Analysis and Systems Development 5/5
- 🔭 I wish to work as a Front End Developer in the future
- ✨ I work as a Network Assistant at the company DIGITALNET

<div align="center">
  <a href="https://github.com/MatheusNxt25">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=MatheusNxt25&show_icons=true&theme=cobalt&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MatheusNxt25&layout=compact&langs_count=7&theme=cobalt"/>
</div>
 
<div style="display: inline_block"><br>
  <img align="center" alt="Matheus-Js" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" >
  <img align="center" alt="Matheus-React" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" >
  <img align="center" alt="Matheus-HTML" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" >
  <img align="center" alt="Matheus-CSS" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" >
  <img align="center" alt="Matheus-figma" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" >
  <img align="center" alt="Matheus-Github" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original-wordmark.svg" >
  <img align="center" alt="Matheus-Vscode" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original-wordmark.svg" >
  <img align="center" alt="Matheus-Java" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" >
  <img align="center" alt="Matheus-MySQL" height="40" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg"/>
</div>
  
##

<div>
    <a href="https://instagram.com/matheusnxt" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the- badge&logo=instagram&logoColor=white" target="_blank"></a>
     <a href="https://www.linkedin.com/in/matheus-oliveira-251a06154/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style =for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
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
          github_user_name: MatheusNxt25
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
