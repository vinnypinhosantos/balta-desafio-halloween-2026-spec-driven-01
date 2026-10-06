# Gerador de Senhas Fortes

## Problema
A maioria dos sites, para atender a requisitos de segurança da informação, solicita a criação de uma senha forte. No entanto, não é natural para o ser humano criar e lembrar de uma sequência grande de números, letras e símbolos.

## Objetivo
Criar um sistema capaz de gerar uma senha forte e recuperar essa senha quando pesquisada a partir de um id.

## Usuários
Pessoas preocupadas com segurança da informação na internet.

## Histórias

### História 1 (H1) - Criar senha
*Como* usuário, 
*quero* gerar uma senha forte,
*para* utilizar em um serviço que exiga essa senha.

### História 2 (H2) - Recuperar identificador
*Como* usuário,
*quero* receber um ID associado à senha gerada
*para* conseguir localizá-la posteriormente.

### História 3 (H3) - Recuperar senha

*Como* usuário,
*quero* pesquisar uma senha utilizando seu ID,
*para* recuperar uma senha que gerei anteriormente.

## Requisitos funcionais

### RF01 — Gerar senha

O sistema deve permitir a geração de uma senha aleatória.

### RF02 — Garantir composição

As senhas deve ter a composição descrita em RN01.

### RF03 — Identificar senha

O sistema deve gerar um ID único para cada senha armazenada.

### RF04 — Armazenar senha

O sistema deve permitir o armazenamento da senha associada ao seu ID.

### RF05 — Consultar senha

O sistema deve permitir a consulta de uma senha a partir do seu ID.

## Regras de negócio

### RN01 - Composição obrigatória

As senhas tem que ter caracteres especiais, pelo menos 16 caracteres e não podem incluir espaços em branco.

### RN02 - Tamanho mínimo

A senha deve possuir um tamanho mínimo de 16 caracteres.

### RN03 - Unicidade do ID

Cada senha armazenada deve possuir um ID único.

### RN04 — Não reutilização do ID

Um ID utilizado para uma senha não deve ser associado a outra senha enquanto existir um registro correspondente.

### RN05 — Senha aleatória

A geração da senha deve utilizar um mecanismo de geração de números aleatórios adequado para geração de credenciais.

### RN06 — Senha não previsível

O algoritmo de geração não deve produzir senhas facilmente previsíveis a partir de senhas anteriormente geradas.

### RN07 — Acesso à senha

Uma senha somente deve ser retornada mediante uma consulta utilizando seu ID.

## Casos de borda

### CB01 — ID inexistente

O usuário pesquisa uma senha utilizando um ID que não existe.

Resultado esperado: o sistema deve informar que nenhuma senha foi encontrada.

### CB02 — ID inválido

O usuário informa um ID em formato inválido.

Resultado esperado: o sistema deve rejeitar a consulta sem realizar uma busca desnecessária no armazenamento.

## Fora de escopo
--

## Critérios de aceite
--