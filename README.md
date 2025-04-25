🎬 MoviesDataSet

Este guia explica como configurar e executar o projeto utilizando Docker e Docker Compose dentro do WSL no Windows.

Antes de começar, verifique se você tem os seguintes itens instalados:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (com integração com WSL habilitada)
- [WSL 2](https://learn.microsoft.com/pt-br/windows/wsl/install)
- Distribuição Linux instalada no WSL (ex: Ubuntu)
- Git (para clonar o repositório)

## ⚙️ Configurando o ambiente

### 1. Verifique se o Docker Desktop está rodando
Abra o Docker Desktop e verifique se ele está em execução.

### 2. Ative a integração do Docker com sua distro WSL
Abra o Docker Desktop:

- Vá em **Settings** > **Resources** > **WSL Integration**
- Ative a integração para a sua distribuição Linux (ex: Ubuntu)

### 3. Clone o repositório

Abra o terminal da sua distro Linux (Ubuntu, por exemplo):

```bash
git clone https://github.com/Edmilson-Jose-FMM/MoviesDataSet.git
cd MoviesDataSet
cd postgredb
```

### 4. Suba os containers
Execute o comando abaixo no terminal do WSL dentro da pasta do projeto:
```bash
   docker-compose up 
```
Esse comando irá:

Construir as imagens (caso não existam)

Criar e rodar os containers definidos no docker-compose.yml

### 5. Verifique se está rodando
Você pode verificar se os serviços estão ativos com:
```bash
docker ps
```
### 6. Motivos pelo uso do Docker
  O uso do docker possibilita com um comando(docker compose up): baixar o arquivo dataset, subir os serviços do banco Postgre, criar a tabela dentro do banco e popular a mesma com via script SQL
