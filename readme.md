# Documentação API projetoBackend

 

Passo a passo:

 

**Criar pasta:**

```

mkdir NOME_DA_PASTA

```

* mkdir serve para criar uma pasta

 

 

**Entrar na pasta:**

```

cd NOME_DA_PASTA

```

* cd serve para entrar na pasta que foi selecionada

 

**Abrir VSCode:**

```

code .

````

 

**Iniciar o gerenciador de pacotes:**

```

npm init -y

```

**Instalar os pacotes:**

 

```

 

npm i express nodemon dotenv

 

```

 

* **express:** Framework web para construção da estrutura da API;

 

* **nodemon:** Monitora as mudanças nos arquivos do projeto e reinicia de forma automática o servidro Node;

 

* **dotenv**: Gerencia as váriaveis do ambiente dentro do projeto.

 

**Criar arquivo gitignore:**

```

touch gitignore

```

<sup> adicionar a pasta node_modules no arquivo .gitignore </sup>

 

* Cria um arquivo vazio

 

```

nano .gitignore

```

 

* **nano** cria um arquivo vazio editável pelo terminal.

 

* **Ctrl + O:** Salvar arquivo;

 

* **Enter:** Confirmar;

 

* **Ctrl + X:** Fechar arquivo.

 

**Adicionar no arquivo .gitignore o nome da pasta criada após a instalação dos pacotes:**

```

Criar estrutura de arquivos e pastas:

```

mkdir src

```

Criar arquivos dentro da pasta src:

```

touch src/app.js

```

Arquivo responsável de criar a configuração da API

```

touch src/server.js

```

Arquivo responsável em receber as configurações da aplicação e rodar a API

```

**Criar pastas dentro da pasta src:**

```

mkdir src/config

```

* Pasta para gerenciar a conexão com o banco de dados

```

mkdir src/controllers

```

* Pasta para gerenciar as requisições das rotas e conexão com banco de dados

```

mkdir src/routes

```

* Pasta para gerenciar as rotas da API

 

**Enviar estrutura do projeto para o gitHub:**

 

 

* Inicializar o gerenciador de arquivos .git

 

```

git init

```

 

* Informar o seu nome e email

 

* Altere o campo 'FIRST_NAME' e coloque o seu nome

 

* Altere o campo 'EMAIL@EXAMPLE.COM' e coloque o seu email do gitHub

```

git config --global user.name "FIRST_NAME"

```

```

 git config --global user.email "EMAIL@EXAMPLE.COM"

 ```

 

 * Verificar arquivos que serão enviados ao gitHub

 

 * Adicionar todos arquivos ao versionamento

 

 ```

 git add .

 ```

 * Salvar projeto e escrever comentário sobre o processo realizado

 

```

git commit -m 'estrutura do projeto'

```

* Criar um novo repositório no gitHub

 

* Clicar no ponto indicado na imagem para copiar a URL do repositório

 

* De volta ao terminal, executar o comando para definir a branch main

 

```

git branch -M main

```

* Informar o repositório que queremos enviar os arquivos

 

* Colar a URL do seu repositório copiada

 

```

git remote add origin COLAR_URL

```

* Enviar os arquivos para o gitHub

 

```

git push -u origin main

```

 

**Atualize a página no gitHub e verifique se os arquivos foram enviados:**

 

* Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina

 

```

cd ..

```

 

* Comando para acessar uma pasta anterior

* Fechar o VSCode com o projeto aberto

 

```

rm -rf projetoBackend

```

 

* rm (remove): comando utilizado para apagar arquivo

* -r (recursive): apaga pastas e subpastas de forma recursiva

* -f (force): não pergunta confirmações

* projetoBackend: nome da pasta que contem os arquivos da aplicação

tem menu de contexto
Redigir

* Para clonar o projeto

```

git clone URL_REPOSITORIO

```

* Acessar a parta

```

cd NOME_REPOSTITORIO

```

* Reinstalar os pacotes da aplicação

```

npm i

```

* Criar arquivo .env na raiz do projeto
* Com o comenado nano, podemos criar e editar um arquivo pelo terminal
* **Ctrl + o:** Salvar o arquivo
* **Enter:** Confirmar
* **Ctrl + x:** Fechar o arquivo

```

nano .env

```

* Digitar no arquivo .env

```

PORT = 3008

```
* Adicionar arquivo .env no .gitignore

```

nano .gitignore

```

```

.env

```

* Abrir o VSCode

```

code .

```

* Criar arquivo de exemplo para as variáveis necessárias da aplicação

```

nano .env.example

```

* Adicionar no arquivo .env.example

```

PORT =

```

* Abrir o aquivo app.js e digitar o cógico

* Importar o pacote express (servidor)

```

const express = require('express');

```

* Importar o pacote dotenv, gerenciador de variáveis de ambiente

```

const dotenv = require('dotenv').config();

```

* Intanciar o express na variável app

```

const app - express();

```

* Setar a porta do servidor a partir do arquivo .env
* O operador condicional '||' significa 'OU', caso não tenha a variável PORT, será utilizado o valor '3333'

```

app.set('port, process,env.PORT || 3333);

```

* Exportar as configurções na variável app

```

modules,exports = app;

```

* Abrir o arquivo server.js e digitar os códigos

* Importar o arquivo app

```

const app = require('./app');

```

* Importar a porta do servidor

```

const port = app.get('port');

```

* Testar API com a função listen
* 1° parâmetro: passamos a porta do servidor
* 2° parâmetro: arrow function para retornar um console informando a porta que está rodando o servidor

```

app.listen(port, () => {
    console.log(`Running on port ${ port}!`);
})

```

* Depois de configurar os pacotes e teste do servidor, vamos criar o comando para executar
* Abrir o arquivo package.json e alterar a chave 'scripts'
* Substituir o comendo 'test' pelo comando 'start' na linha 7

```

"start":"nodemon src/server.js"

```

* Rodar o comando no terminal com gitBash

```

npm run start

```

* Atualizar projeto no gitHub
* Adicionar todos arquivos ao versionamento

```

git add.

```

* Salvar projeto e escrever comentários sobre o processo realizado

```

git commit -m 'configuração do projeto

```

* Enviar os arquivos atualizaos para o gitHub

```

git push

```

* Atualize a página no gitHub e verifique se os aruivos foram atualizados
* Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina

```

cd ..

```

* Comando para acessar uma pasta anterior
* Fechar o VSCode com o projeto aberto 

```

rm -rf projetoBackend

```

* rm (remove): comando utilizado para apagar arquivo

* -r (recursive): apaga pastas e subpastas de forma recursiva

* -f (force): não pergunta confirmações

* projetoBackend: nome da pasta que contem os arquivos da aplicação