# MEU-PROJETO-JAVA


 ⚙️ **Requisitos Técnicos Obrigatórios**

1. **Manipulação do DOM**

  * A navegação entre seções ocorre **sem recarregar a página**.
  * Cada “página” é renderizada dinamicamente via JavaScript.
* Criar um **sistema de templates JavaScript**:

  * Por exemplo, armazenar o HTML de cada “página” como template string no JS.
  * Renderizar o conteúdo conforme o usuário navega.

**Exemplo  de template SPA:**

```js
const routes = {
  home: "<h1>Bem-vindo à Home</h1>",
  about: "<h1>Sobre nós</h1>",
  contact: "<h1>Contato</h1>"
};

function navigateTo(page) {
  document.getElementById("app").innerHTML = routes[page];
}

document.querySelectorAll("nav a").forEach(link => {
  link.addEventListener("click", e => {
    e.preventDefault();
    navigateTo(e.target.dataset.page);
  });
});
```

---

 2. Verificação de Consistência de Dados

* Criar um **sistema de validação de formulários**:

  * Verificar se todos os campos obrigatórios estão preenchidos.
  * Validar e-mails, senhas, números, etc.
  * Exibir mensagens visuais de erro (ex: `span` com aviso, bordas vermelhas).




*Exemplo :

```js
const form = document.querySelector("form");
form.addEventListener("submit", e => {
  e.preventDefault();

  const email = form.email.value.trim();
  const password = form.password.value.trim();

  if (!email.includes("@")) {
    alert("E-mail inválido!");
    return;
  }

  if (password.length < 6) {
    alert("A senha deve ter pelo menos 6 caracteres.");
    return;
  }

  alert("Formulário enviado com sucesso!");
});
```







meu-projeto/
│
├── index.html
├── css/
│   └── style.css
├── js/
│   ├── main.js          # ponto de entrada
│   ├── spa.js           # controle das rotas e templates
│   ├── formValidation.js # validação de formulários
│   └── storage.js        # manipulação de localStorage (opcional)
└── img/
    └── logo.png



Quer que eu monte esse **modelo completo de projeto** (HTML, CSS e JS modularizado) para você usar como base?
