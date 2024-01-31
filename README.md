<h1>Jogo do número secreto</h1>

<h2>�� Sobre</h2>
<p>Projeto utilizado nos cursos de lógica de programação da Alura.</p>

## �� Tecnologias
<div>
  <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
</div>

🔭 I’m currently working on ...
🌱 I’m currently learning ...
👯 I’m looking to collaborate on ...
🤔 I’m looking for help with ...
💬 Ask me about ...
📫 How to reach me: ...
😄 Pronouns: ...
⚡ Fun fact: ...

<div>
<a href="https://www.youtube.com/seu-canal-youtube-aqui" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
<a href="https://instagram.com/seu-usuário-instagram-aqui" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href="https://www.twitch.tv/seu-usuário-aqui" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
<a href = "mailto:contato@seu-usuário-aqui"><img loading="lazy" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/seu-usuário-linkedln-aqui" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40"/>


<div>
<a href="https://github.com/seu-usuário-aqui">
<img loading="lazy" height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=seu-usuário-aqui&layout=compact&langs_count=7&theme=dracula"/>
<img loading="lazy" height="180em" src="https://github-readme-stats.vercel.app/api?username=seu-usuário-aqui&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
</div>


![Snake animation](https://github.com/seu-usuário-aqui/seu-usuário-aqui/blob/output/github-contribution-grid-snake.svg)

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
          github_user_name: seu-usuário-aqui
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
