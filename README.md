# TodoListDockerAula

## Introdução

Este projeto é uma aplicação Todo List (lista de tarefas) containerizada usando Docker, desenvolvida com propósitos educacionais. Ele demonstra como empacotar uma aplicação web em contêineres e orquestrá-los por meio do Docker Compose. Com isso, é possível executar facilmente todos os serviços necessários de forma isolada, simplificando a configuração e o ambiente de desenvolvimento.

## Clonando o Repositório

Para obter uma cópia do projeto em sua máquina local, você deve clonar este repositório. Caso ainda não tenha feito, abra um terminal e execute os comandos de clone.

```bash
git clone https://github.com/maiconda/TodoListDockerAula
```

Após clonar o repositório, navegue até o diretório do projeto

```bash
cd TodoListDockerAula
```

## Iniciando o Projeto com Docker

Certifique-se de ter o Docker e o Docker Compose instalados em seu sistema. Dentro do diretório do projeto clonado, você pode iniciar todos os serviços (aplicação web e banco de dados, se houver) usando o Docker Compose. Para isso, execute o comando:

```bash
docker compose up -d --build
```
- --build: Faz com que a imagem seja construida antes de inicar os containers.
- -d: Faz com que os containers executem de e deixe o terminal indepentente.

## Acessando a aplicação

Após a execução o projeto estará disponível nas seguintes portas:

- 80: Porta HTTP padrão, configurada para redirecionar automaticamente para HTTPS.
- 443: Porta HTTPS onde a aplicação estará realmente acessível.

Abra o navegador e acesse:

```bash
https://localhost
```

## Parando o Projeto com Docker

Para parar o projeto no docker, execute o seguinte comando:

```bash
docker compose down
```

Para limpar imagens de containers não utilizados, execute o seguinte comando:

```bash
docker image prune -f
```
- -f: Faz com que o comando seja executado a "força", ou seja, sem perguntar confirmação.

## Comandos úteis

### Verificação de containers ativos

Para listar os cointainers ativos no projeto, execute o comando:

```bash
docker compose ps
```

Para listar todos, execute o comando:

```bash
docker ps
```

### Visualização de Logs

Exibir todos os logs completos do projeto:

```bash
docker compose logs
```

Acompanhar logs em tempo real:

```bash
docker compose logs -f
```