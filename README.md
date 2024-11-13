# AULA 03

# ALUNO: Albert
# TURMA: 109

**1. Criação do "package.json"**:
  -   # Passo a Passo: Configuração Básica do Node e NPM para um Projeto

Este tutorial explica como configurar um projeto básico em Node.js, instalar o `lite-server` e integrar o projeto com o Git.

## Objetivos

Ao final deste exercício, você será capaz de:
1. Configurar o arquivo `package.json` para um projeto Node.js.
2. Instalar um módulo NPM (`lite-server`) e utilizá-lo no projeto.
3. Configurar o `.gitignore` para ignorar a pasta `node_modules` e preparar o projeto para envio ao repositório.

## Requisitos

- Node.js e NPM instalados
- Git configurado

## 1. Inicializando o `package.json`

1. No terminal, navegue até a pasta do seu projeto (`git-test`).
2. Digite o seguinte comando para inicializar o `package.json`:

   npm init
Siga as instruções no prompt:

Aceite os valores padrões para a maioria das entradas.
Defina o ponto de entrada como index.html (ao invés de index.js).
Isso criará um arquivo package.json com as configurações iniciais do seu projeto.

# 2. Instalando o lite-server
 - No terminal, instale o lite-server como uma dependência de desenvolvimento:

npm install lite-server --save-dev
Este servidor de desenvolvimento ajudará a atualizar automaticamente a página ao fazer alterações.

 - Abra o arquivo package.json no editor de texto e adicione as seguintes linhas no campo scripts:

"scripts": { 
  "start": "npm run lite", 
  "test": "echo \"Error: no test specified\" && exit 1", 
  "lite": "lite-server" 
},
No mesmo arquivo, adicione as seguintes informações para o repositório, autor e descrição do projeto:

json
Copiar código
"repository": { 
  "type": "git", 
  "url": "git+https://github.com/<user>/<repository_path>" 
},
"author": "", 
"license": "ISC", 
"homepage": "https://github.com/<user>/<repository_path>", 
"description": "This is the Git and Node basic learning project",

# 3. Iniciar o Servidor de Desenvolvimento
 - Inicie o servidor com o comando:

npm start
Isso abrirá a página index.html em seu navegador.

Faça alterações na página index.html em um editor e salve. O navegador atualizará automaticamente para refletir as mudanças.

# 4. Configuração do .gitignore
 - No diretório do projeto, crie um arquivo chamado .gitignore (o nome deve começar com um ponto).
Dentro do arquivo .gitignore, adicione o seguinte conteúdo:

node_modules
Isso evita que a pasta node_modules seja adicionada ao seu repositório Git, economizando espaço e evitando a necessidade de enviar os pacotes instalados.

# 5. Comitar e Enviar para o Git
 - No terminal, execute o comando para adicionar todos os arquivos (exceto node_modules) ao commit:

git add .
Em seguida, faça o commit:
bash
Copiar código
git commit -m "Configuração inicial do projeto Node com lite-server"

 - Por fim, envie para o repositório remoto:

git push origin main
