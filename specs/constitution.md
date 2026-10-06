# Constituição do projeto

## Stack
* Java 25
* Spring Boot
* Maven
* SQLite com Hibernate
* JUnit
* Swagger/OpenAPI

## Arquitetura
O projeto é uma API Rest. A ideia é termos um controller por onde entram a requisição e ele retorna uma resposta. O controller vai receber um DTO e retornar um DTO e um Status HTPP. O controller não deve acessar dados diretamente. O controller não deve possuir regras de negócio. As regras de negócios devem estar nos services em métodos com apenas uma responsabilidade. O service não deve receber nem retornar requisições HTTP. O service não terá acesso ao banco de dados, apenas fará validações e aplicará as regras de negócios. A responsabilidade de conhecer o esquema de dados é do Repository, que apenas fará isso.

## Qualidade
Todos os métodos com regra de negócio devem ter pelo menos um teste de unidade com casos de sucesso e de exceção. Todos os endpoints devem possuir testes de integração. O uso de tipos primitivos no código não pode ser exagerado, quando o dado possui validações inerentes à ele e não à regra de negócio desenvolvida, deve ser criado um tipo específico para reutilização.

## Convenções
* Pacotes: Escritos apenas com letras minúsculas (ex: br.com.empresa.projeto).
* Classes e Interfaces: Usam CamelCase com a primeira letra maiúscula e nomes que representam substantivos (ex: ClienteService, Pagamento).
* Métodos: Usam camelCase começando com letra minúscula e nomes que indicam verbos ou ações (ex: calcularTotal(), salvarCliente()).
* Constantes: Escritas inteiramente em letras maiúsculas, com palavras separadas por underline (ex: VALOR_MAXIMO).
* Indentação: 4 espaços por nível de bloco (não misturar tabs e espaços).
* Utilizar UTF-8 para os caracteres.
* Data e hora devem estar em UTC.

## Governança
* O projeto deve utilizar o gitflow de forma básica: branches main, develop e as branchs por feature (padrão feature-descricao-da-tarefa). Cada nova feature deriva da branch develop e ao realizar a tarefa deve ser feito um pull request de volta para develop.
* Realizar análise estática dos arquivos modificados em cada funcionalidade desenvolvida.
