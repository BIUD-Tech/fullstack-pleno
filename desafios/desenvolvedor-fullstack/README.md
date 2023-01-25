# Desafio Fullstack Software Developer - BIUD

Nesse desafio você construirá uma versão bastante simplificada de um dashboard de transações de compra de produtos. O objetivo é avaliar suas habilidades com desenvolvimento web, arquitetura de software e boas práticas de programação.

## Contexto

Em sua essência um dashboard tem duas funções muito importantes:

1. Agregar dados das empresas
2. Apresentar relatórios e dashboards para que os gestores possam tomar decisões

Na BIUD, nós temos três (entre várias) entidades que representam essas informações:

* `purchases`: que representam as informações da compra, data, valor, descontos, etc
* `products`: que representam os os produtos vendidos
* `customers`: que representam os clientes que compraram os produtos

> Nota: quando uma compra é processada o segundo envio de uma compra com a mesma chave é ignorado, ou seja, não é possível ter duas compras com o mesmo código de referência.

## Requisitos

Você deve criar um serviço (REST ou GraphQL) com os seguintes requisitos:

1. O serviço deve processar compras através de um endpoint, recebendo as seguintes informações:
    * Código de referência da compra
    * Descontos
    * Valor
    * Data
    * Produtos (nome, quantidades e valor unitário)
    * Cliente (nome, email, CPF)
    * Observações. Ex: `'Produto enviado para o cliente por SEDEX'`
2. O serviço deve permitir que o usuário possa consultar as compras através de um endpoint, filtrando por:
    * Código de referência da compra
    * Cliente (nome, email, CPF)
    * Data
    * Valor
3. O serviço deve trazer dados agregados sobre as compras, como por exemplo:
    * Quantidade de compras
    * Valor total de compras
    * Valor médio de compras
    * Valor total de descontos
    * Valor médio de descontos
    * Valor total de produtos
    * Valor médio de produtos
    * Valor total de compras por cliente
    * Valor médio de compras por cliente
    * Valor total de compras por produto
    * Valor médio de compras por produto
4. Criar um frontend, utilizando um framework javascript, que mostre um dashboard com os dados agregados das compras e listagem com busca de compras utilizando os filtros listados no item 2
5. Integrar o seu serviço com algum ERP, SaaS ou plataforma opensource de e-commerce, exemplo: Shopify, Magento, WooCommerce, etc. Você pode usar uma conta de teste para isso.
> Nota: neste desafio, você não precisa se preocupar com dados de pagamento ou qualquer outra informação não informada anteriormente.

> Nota 2: Ao processar uma compra no Saas/ERP escolhido você deve enviar os dados para o serviço que você criou.

## Restrições

1. O serviço deve ser escrito em PHP frameworks Symfony ou Laravel. Aqui na BIUD usamos Symfony
2. O serviço deve armazenar informações em um banco de dados. Você pode escolher o banco que achar melhor. Aqui na BIUD usamos PostgreSQL
3. O projeto deve ter um README.md com todas as instruções sobre como executar e testar o projeto e os serviços disponibilizados.
4. O frontend deve ser escrito utilizando ReactJS, Angular ou VueJS. Aqui na BIUD usamos React


## Diferenciais

1. Testes automatizados são bem vindos.
2. O serviço deve ser executado em um ambiente de desenvolvimento (Docker, Vagrant, etc).
3. Apreciamos boa documentação e boas práticas de programação.
4. Adoramos código limpo e bem escrito.
5. DDD, TDD, SOLID, Clean Code, Command Bus, GraphQL, Design Patterns, etc.
6. Utilizar o Github para versionar o projeto.
7. Brokers de mensagens (RabbitMQ, Kafka, etc).


## Avaliação

1. O desafio deve ser enviado para a pessoa do RH que estiver em contato com você, no formato de `.zip` ou um link para um repositório do Github
2. Iremos te avaliar pela arquitetura do serviço, qualidade do código, entendimento das regras de negócio, capricho com o desafio e o quão preparado esse serviço estaria para ser rodado em produção
3. Depois que corrigirmos o desafio, te chamaremos para conversar com o time, apresentar o desafio e discutir sobre as decisões que você tomou
4. Achamos que **1 semana** é um tempo ok para fazer o desafio, mas sabemos que nem todo mundo tem o mesmo nível de disponibilidade. Portanto, nos avise se precisar de mais tempo, ok?
5. Boa sorte :)