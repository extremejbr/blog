# Teste Melhor Envio

Repositório referente ao Teste de DevOps para a empresa Melhor Envio.

## Time responsável:

Jones Radtke - DevOps

## Descrição

O projeto está estruturado em 4 containers Docker.

* APP - Responsável com disponbilizar o código do projeto;
* WEB - Resposável pelo serviço de página da aplicação; 
* DATABSE - Responsável pelo serviço de danco de dados MySQL do projeto;
* REDIS - Responsável por efetuar o sistemna de cache da aplicação.


## Requisitos

* Docker - https://www.docker.com/
* Docker Composer - https://docs.docker.com/compose/

### Efetuar os seguintes passos para inicializar a aplicação:

1. Build do projeto com Docker Composer.

`$ docker-cpmpose build`

2. Iniciar os containers do projeto.

`$ docker-compose up -d`

3. Copiar o arquivo .env.example na raíz e nomeá-lo .env na raiz do containner APP.

`$ docker-compose exec app mv .env.example .env`

4. Instaalar as dependências do projeto.

`$ docker-compose exec app composer update`

5. Gerar uma nova chave para a aplicação Laravel.

`$ docker-compose exec app php artisan key:generate `

6. A aplicação estará disponível no endpoint
 'http://localhost:8080'

