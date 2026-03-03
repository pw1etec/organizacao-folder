# 💻 Atividade Prática – Organização de Estrutura em Bash

## 🎯 Objetivo

Criar via Terminal Bash a estrutura de diretórios e arquivos da empresa fictícia **DevTech Solutions**, simulando um ambiente real de organização de projetos em servidor Linux.

---

## 📌 Regras Importantes

* Utilizar obrigatoriamente:

  * `mkdir -p`
  * `touch`
  * `cd`
  * `echo`
  * `cp -r`
* Não utilizar interface gráfica.
* Todos os comandos utilizados devem estar registrados em um único arquivo.
* O arquivo deve se chamar:

```
setup-devtech.sh
```

* O arquivo deve ser enviado na atividade do **Google Classroom**.

---

## 📂 Estrutura Obrigatória

```
devtech/
│
├── projetos/
│   ├── site-institucional/
│   │   ├── src/
│   │   │   ├── css/
│   │   │   ├── js/
│   │   │   └── img/
│   │   ├── public/
│   │   │   └── index.html
│   │   └── README.md
│   │
│   └── sistema-interno/
│       ├── backend/
│       │   ├── src/
│       │   │   ├── controllers/
│       │   │   ├── models/
│       │   │   └── routes/
│       │   └── server.js
│       │
│       └── frontend/
│           ├── src/
│           │   ├── components/
│           │   ├── pages/
│           │   └── services/
│           └── index.html
│
├── financeiro/
│   ├── 2025/
│   │   ├── janeiro.txt
│   │   ├── fevereiro.txt
│   │   └── marco.txt
│   └── relatorio-anual.txt
│
├── RH/
│   ├── funcionarios.txt
│   └── contratacoes-2025.txt
│
└── docs/
    ├── contratos/
    └── manuais/
```

---

## 📝 Parte Obrigatória

Após criar a estrutura, o script deve:

* Criar todos os arquivos indicados
* Inserir conteúdo básico em:

  * README.md
  * server.js
  * index.html (ambos)
  * funcionarios.txt
  * relatorio-anual.txt

---

## 💾 Backup Obrigatório

O script deve criar uma cópia completa da pasta:

```
sistema-interno
```

Com o nome:

```
sistema-interno-backup
```

---

## 📤 Entrega

Enviar o arquivo:

```
setup-devtech.sh
```

Na atividade correspondente no Google Classroom.

---

# 🎓 Dica Pedagógica Para Você

Quando alguém perguntar:

> “Professor, é para rodar?”

Você responde:

> “Sim. Um script que não executa não é um script.”

Isso já eleva o nível da turma automaticamente 😎

---

Se você quiser, posso agora:

* 📊 Criar rubrica de correção (com pontuação automática)
* 🧪 Criar versão avaliativa valendo nota
* 🧠 Criar armadilhas pedagógicas para testar se copiaram
* 🚀 Criar versão nível avançado com permissões (`chmod`, `chown`)

Qual próximo passo, professor? 😎
