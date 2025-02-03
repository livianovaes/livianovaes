# <span style="color: red;">HELLO WORLD</span> <span class="typewriter"></span>

## 👋 Olá, eu sou Lívia Novaes!

- 🎓 Cursando Engenharia Mecatrônica e Análise e Desenvolvimento de Sistemas.
- 🎮 Amante da tecnologia e aspirante à pro player em jogos online!
- 🌟 Apaixonada por desenvolvimento web e programação.

## 🛠️ Tecnologias Dominadas

Aqui estão algumas das tecnologias que eu domino:

![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Java](https://img.shields.io/badge/-Java-007396?style=flat-square&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white)

## 📂 Meus Repositórios no GitHub

Aqui estão alguns dos meus repositórios mais recentes:

<div id="repos"></div>

## 📫 Contato

- [LinkedIn](https://www.linkedin.com/in/lívia-novaes-65ba982b8/)
- Email: liviajfnovaes15@gmail.com

<script>
  // Efeito de typewriting no título
  const typewriterText = "HELLO WORLD";
  const typewriterElement = document.querySelector('.typewriter');
  let i = 0;

  function typeWriter() {
    if (i < typewriterText.length) {
      typewriterElement.innerHTML += typewriterText.charAt(i);
      i++;
      setTimeout(typeWriter, 100);
    }
  }

  typeWriter();

  // Integração com a API do GitHub
  fetch('https://api.github.com/users/seu-usuario/repos?sort=updated&per_page=5')
    .then(response => response.json())
    .then(data => {
      const reposElement = document.getElementById('repos');
      data.forEach(repo => {
        const repoElement = document.createElement('div');
        repoElement.innerHTML = `
          <h3><a href="${repo.html_url}" target="_blank">${repo.name}</a></h3>
          <p>${repo.description || 'Sem descrição'}</p>
          <p>⭐ ${repo.stargazers_count} | 🍴 ${repo.forks_count}</p>
        `;
        reposElement.appendChild(repoElement);
      });
    })
    .catch(error => console.error('Erro ao carregar repositórios:', error));
</script>
