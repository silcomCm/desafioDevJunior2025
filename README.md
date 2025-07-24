# Desafio Técnico: Sistema MRP Simples (Bicicletas e Computadores)

## Contexto
Sua empresa fabrica bicicletas e computadores. Para garantir que a produção não pare por falta de componentes, você precisa de um sistema simples de MRP (Material Requirements Planning).

## Componentes necessários

### Bicicleta:
- 2 rodas
- 1 quadro
- 1 guidão

### Computador:
- 1 gabinete
- 1 placa-mãe
- 2 pentes de memória RAM

## Objetivo
Desenvolva uma aplicação web simples que permita:

### 1. Cadastro de Estoque:
Uma página para inserir e atualizar o estoque atual de cada componente (rodas, quadros, guidões, gabinetes, placas-mãe, memórias RAM). Os dados devem ser salvos em um banco de dados.

### 2. Página de MRP:
Uma página onde o usuário informa quantas bicicletas e computadores deseja montar.

Ao submeter, o sistema deve consultar o estoque no banco de dados e exibir, para cada componente, uma tabela detalhada com as seguintes colunas:
- **Componente**
- **Quantidade necessária** (para a produção informada)
- **Quantidade em estoque**
- **Quantidade retirada do estoque** (igual à quantidade necessária, limitado ao estoque disponível)
- **Quantidade a comprar** (se faltar, mostrar quanto precisa comprar; se não faltar, mostrar zero)

O cálculo deve ser feito dinamicamente, com base na quantidade informada pelo usuário e no estoque atual.

## Exemplo de Fluxo

### 1. Usuário acessa a página de estoque e cadastra:
- Rodas: 10
- Quadros: 5
- Guidões: 10
- Gabinetes: 2
- Placas-mãe: 5
- Memórias RAM: 6

### 2. Usuário acessa a página de MRP, informa:
- Bicicletas a montar: 4
- Computadores a montar: 3

### 3. O sistema exibe uma tabela assim:

| Produto | Componente | Necessário | Em estoque | Retirado do estoque | A comprar |
|---------|------------|------------|------------|---------------------|-----------|
| Bicicleta | Rodas | 8 | 10 | 8 | 0 |
| Bicicleta | Quadros | 4 | 5 | 4 | 0 |
| Bicicleta | Guidões | 4 | 10 | 4 | 0 |
| Computador | Gabinetes | 3 | 2 | 2 | 1 |
| Computador | Placas-mãe | 3 | 5 | 3 | 0 |
| Computador | Memórias RAM | 6 | 6 | 6 | 0 |

## Requisitos Técnicos
- O sistema deve ser web (pode ser feito em qualquer framework ou linguagem)
- O banco de dados pode ser MySQL, PostgreSQL ou SQLite
- O código deve ser organizado e conter instruções de como rodar o projeto
- O cálculo do MRP deve ser feito dinamicamente, consultando os dados salvos no banco

## Critérios de Avaliação
- **Funcionalidade**: O sistema atende aos requisitos especificados
- **Organização do código**: Estrutura clara e bem documentada
- **Interface**: Usabilidade e apresentação das informações
- **Banco de dados**: Modelagem adequada e consultas eficientes
- **Documentação**: Instruções claras para execução do projeto

## Entrega
- Código fonte completo
- Script de criação do banco de dados 
- Arquivo README com instruções de instalação e execução
- Prazo sugerido: 3-5 dias