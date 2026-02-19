# Aula – Terminal e Linha de Comando (CLI)

## 📌 O que é CLI?

CLI significa Command Line Interface (Interface de Linha de Comando).

É uma forma de interagir com o sistema operacional por meio de comandos digitados, sem uso de interface gráfica.

Antes dos sistemas com janelas, todo computador era controlado pelo terminal.
Hoje, desenvolvedores utilizam CLI porque:

* É mais rápida que interface gráfica
* Permite automação
* Facilita gerenciamento de projetos
* É padrão em servidores e ambientes profissionais
* Dá controle total do sistema

Dois ambientes que usaremos:

* CMD (Prompt de Comando do Windows)
* Git Bash (Terminal estilo Linux para Windows)

---

# 1️⃣ Navegação entre Pastas

| Ação                | CMD           | Git Bash      | Exemplo de Uso | O que acontece                   |
| ------------------- | ------------- | ------------- | -------------- | -------------------------------- |
| Mostrar pasta atual | `cd`          | `pwd`         | `pwd`          | Mostra onde você está no sistema |
| Listar arquivos     | `dir`         | `ls`          | `ls`           | Lista arquivos da pasta atual    |
| Entrar em pasta     | `cd projetos` | `cd projetos` | `cd aula`      | Entra na pasta chamada aula      |
| Voltar pasta        | `cd ..`       | `cd ..`       | `cd ..`        | Volta um nível na estrutura      |
| Limpar tela         | `cls`         | `clear`       | `cls`          | Limpa o terminal                 |

---

# 2️⃣ Criando e Organizando Pastas

| Ação                | CMD              | Git Bash         | Exemplo          | Resultado                 |
| ------------------- | ---------------- | ---------------- | ---------------- | ------------------------- |
| Criar pasta         | `mkdir nome`     | `mkdir nome`     | `mkdir projeto`  | Cria pasta projeto        |
| Criar várias pastas | `mkdir src docs` | `mkdir src docs` | `mkdir src docs` | Cria duas pastas          |
| Ver estrutura       | `tree`           | `tree`           | `tree`           | Mostra organização visual |

---

# 3️⃣ Trabalhando com Arquivos

| Ação           | CMD                    | Git Bash                 | Exemplo                     | Resultado              |
| -------------- | ---------------------- | ------------------------ | --------------------------- | ---------------------- |
| Criar arquivo  | `echo texto > arq.txt` | `echo "texto" > arq.txt` | `echo Olá > teste.txt`      | Cria arquivo com texto |
| Ler arquivo    | `type arq.txt`         | `cat arq.txt`            | `type teste.txt`            | Mostra conteúdo        |
| Copiar arquivo | `copy a.txt b.txt`     | `cp a.txt b.txt`         | `copy teste.txt copia.txt`  | Cria cópia             |
| Renomear       | `rename a.txt b.txt`   | `mv a.txt b.txt`         | `rename teste.txt novo.txt` | Altera nome            |
| Excluir        | `del arq.txt`          | `rm arq.txt`             | `del copia.txt`             | Remove arquivo         |

---

# 4️⃣ Editando Arquivos

| Ação                 | CMD                   | Git Bash           | Exemplo             |
| -------------------- | --------------------- | ------------------ | ------------------- |
| Abrir bloco de notas | `notepad arquivo.txt` | —                  | `notepad teste.txt` |
| Editar no terminal   | —                     | `nano arquivo.txt` | `nano teste.txt`    |

---

# 5️⃣ Executando Programas

| Ação            | Comando         | Exemplo         | Resultado              |
| --------------- | --------------- | --------------- | ---------------------- |
| Executar JS     | `node app.js`   | `node app.js`   | Roda código JavaScript |
| Executar Python | `python app.py` | `python app.py` | Roda script Python     |
| Executar .bat   | `arquivo.bat`   | `meuscript.bat` | Executa script Windows |

---

# 📌 Comandos Utilizados em Arquivos .BAT

| Comando               | Exemplo                 | O que faz                                                                             |
| --------------------- | ----------------------- | ------------------------------------------------------------------------------------- |
| `@echo off`           | `@echo off`             | Oculta a exibição dos comandos enquanto o script executa (deixa mais “profissional”). |
| `echo`                | `echo Olá Mundo`        | Exibe uma mensagem na tela.                                                           |
| `echo > arquivo.txt`  | `echo Texto > log.txt`  | Cria arquivo e escreve conteúdo (sobrescreve).                                        |
| `echo >> arquivo.txt` | `echo Novo >> log.txt`  | Adiciona conteúdo ao final do arquivo.                                                |
| `pause`               | `pause`                 | Pausa a execução e espera o usuário pressionar uma tecla.                             |
| `color`               | `color 0A`              | Muda a cor do terminal (fundo e texto).                                               |
| `cls`                 | `cls`                   | Limpa a tela.                                                                         |
| `title`               | `title Sistema Interno` | Altera o título da janela do terminal.                                                |
| `timeout`             | `timeout /t 3`          | Aguarda alguns segundos antes de continuar.                                           |
| `mkdir`               | `mkdir pasta`           | Cria diretório.                                                                       |
| `cd`                  | `cd pasta`              | Entra na pasta especificada.                                                          |
| `%date%`              | `echo %date%`           | Mostra data atual do sistema.                                                         |
| `%time%`              | `echo %time%`           | Mostra horário atual.                                                                 |
| `%username%`          | `echo %username%`       | Mostra usuário logado no Windows.                                                     |
| `if`                  | `if exist arquivo.txt`  | Executa condição lógica.                                                              |

---

# 📌 Exemplo Comentado de Script .BAT

Arquivo: sistema.bat

```
@echo off
title Sistema Interno
color 0A
cls

echo Iniciando sistema...
timeout /t 2

echo Usuario logado: %username%
echo Data: %date%
echo Hora: %time%

echo Criando pasta relatorios...
mkdir relatorios

echo Processo finalizado!
pause
```

---

# 📌 Exemplo com Estrutura Condicional

Arquivo: verificador.bat

```
@echo off
cls

if exist dados.txt (
    echo Arquivo encontrado!
) else (
    echo Arquivo nao encontrado!
)

pause
```

Aqui você já introduz lógica de programação dentro do terminal.

---

# 📌 Exemplo Interativo com Entrada do Usuário

Arquivo: login.bat

```
@echo off
cls

set /p nome=Digite seu nome: 
echo Bem-vindo %nome%!
pause
```

Comando novo explicado:

`set /p` → permite capturar entrada digitada pelo usuário.

---

Agora a parte que impressiona.

Arquivos .bat são scripts executáveis do Windows.

Para criar:

1. Criar arquivo:
   notepad sistema.bat
2. Salvar como:
   sistema.bat

---

## 🟢 Script 1 – Simulador Hacker

Conteúdo:

```
@echo off
color 0A
echo Iniciando sistema...
timeout /t 2
echo Conectando ao servidor...
timeout /t 2
echo Acesso autorizado!
pause
```

O que faz:

* Muda cor do terminal
* Simula carregamento
* Pausa no final

---

## 🔵 Script 2 – Criador de Estrutura de Projeto

```
@echo off
echo Criando estrutura de projeto...
mkdir projeto
cd projeto
mkdir src
mkdir docs
echo Projeto criado com sucesso!
pause
```

Automatiza criação de pastas.

---

## 🟣 Script 3 – Gerador de Relatório

```
@echo off
echo Gerando relatorio...
echo Relatorio do Sistema > relatorio.txt
echo Data: %date% >> relatorio.txt
echo Hora: %time% >> relatorio.txt
echo Usuario: %username% >> relatorio.txt
echo Relatorio criado!
pause
```

Cria arquivo automático com dados do sistema.

---

# 🎯 Desafio Final

Criar um .bat que:

1. Crie pasta chamada empresa
2. Dentro dela crie: financeiro, rh e ti
3. Gere um arquivo info.txt com data e hora
4. Mostre mensagem final personalizada

---
