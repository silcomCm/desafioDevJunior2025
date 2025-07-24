# 🏭 Desafio Técnico: Sistema MRP Simples
**Planejamento de Necessidades de Materiais para Fábrica de Bicicletas e Computadores**

---

## 📋 **Visão Geral do Projeto**

Você é responsável por desenvolver um sistema web de **MRP (Material Requirements Planning)** para uma empresa que fabrica dois produtos: **bicicletas** e **computadores**. O sistema deve calcular automaticamente as necessidades de compra de componentes com base na produção planejada e no estoque atual.

### **Problema a Resolver**
A empresa precisa saber exatamente quais componentes comprar para atender uma demanda de produção específica, evitando paradas na linha de montagem por falta de materiais.

---

## 🔧 **Especificação dos Produtos**

### **Bicicleta** (1 unidade requer):
- **2** rodas
- **1** quadro  
- **1** guidão

### **Computador** (1 unidade requer):
- **1** gabinete
- **1** placa-mãe
- **2** pentes de memória RAM

---

## 🎯 **Funcionalidades Obrigatórias**

### **1. Módulo de Gerenciamento de Estoque**
**Página:** `/estoque`

**Funcionalidades:**
- Cadastrar quantidade inicial de cada componente
- Atualizar estoque atual de componentes existentes
- Visualizar estoque atual de todos os componentes
- Persistir dados no banco de dados

**Componentes a gerenciar:**
- Rodas
- Quadros
- Guidões
- Gabinetes
- Placas-mãe
- Memórias RAM

### **2. Módulo de Planejamento MRP**
**Página:** `/mrp`

**Funcionalidades:**
- Formulário para inserir quantidade desejada de:
  - Bicicletas a montar
  - Computadores a montar
- Calcular necessidades de materiais automaticamente
- Indicar exatamente quanto comprar de cada componente

---


## 💡 **Exemplo Prático Completo**

### **Cenário Inicial - Estoque Cadastrado:**
```
Rodas: 10 unidades
Quadros: 5 unidades  
Guidões: 10 unidades
Gabinetes: 2 unidades
Placas-mãe: 5 unidades
Memórias RAM: 6 unidades
```

### **Solicitação de Produção:**
- **4 bicicletas**
- **3 computadores**

### **Cálculos Automáticos:**

**Para Bicicletas (4 unidades):**
- Rodas necessárias: 4 × 2 = **8 rodas**
- Quadros necessários: 4 × 1 = **4 quadros**  
- Guidões necessários: 4 × 1 = **4 guidões**

**Para Computadores (3 unidades):**
- Gabinetes necessários: 3 × 1 = **3 gabinetes**
- Placas-mãe necessárias: 3 × 1 = **3 placas-mãe**
- Memórias RAM necessárias: 3 × 2 = **6 memórias**

### **Tela do MRP Esperada:**

| Produto | Componente | Necessário | Em Estoque | Retirado do Estoque | A Comprar |
|---------|------------|------------|------------|---------------------|-----------|
| Bicicleta | Rodas | 8 | 10 | 8 | **0** |
| Bicicleta | Quadros | 4 | 5 | 4 | **0** |
| Bicicleta | Guidões | 4 | 10 | 4 | **0** |
| Computador | Gabinetes | 3 | 2 | 2 | **1** ⚠️ |
| Computador | Placas-mãe | 3 | 5 | 3 | **0** |
| Computador | Memórias RAM | 6 | 6 | 6 | **0** |

**Resultado:** É necessário comprar **1 gabinete** para completar a produção.

---

## 🛠️ **Requisitos Técnicos**

### **Tecnologias Aceitas**
- **Backend:** Pode ser feito em qualquer framework ou linguagem
- **Frontend:** HTML/CSS/JavaScript, React, Vue, Angular, ou framework de sua escolha
- **Banco de Dados:** MySQL, PostgreSQL, SQLite

### **Arquitetura Mínima**
- Separação clara entre frontend e backend
- Tratamento de erros básico

### **Funcionalidades Técnicas**
- ✅ Operações CRUD para estoque
- ✅ Cálculos dinâmicos de MRP
- ✅ Persistência em banco de dados
- ✅ Validação de dados de entrada

---

## 📁 **Estrutura de Entrega**

### **Arquivos Obrigatórios:**
```
projeto-mrp/
├── README.md                 # Instruções completas
├── database/
│   └── schema.sql           # Script de criação do banco
├── src/                     # Código fonte
└── docs/                    # Documentação adicional (opcional)
```

### **Conteúdo do README.md:**
1. **Pré-requisitos** (versões de software necessárias)
2. **Instalação** (passo a passo)
3. **Configuração do banco de dados**
4. **Como executar o projeto**
5. **Como usar o sistema**
6. **Estrutura do projeto**

---

## 🎯 **Critérios de Avaliação**

### **Funcionalidade (40%)**
- ✅ Sistema atende todos os requisitos especificados
- ✅ Cálculos de MRP estão corretos
- ✅ Persistência de dados funciona adequadamente
- ✅ Interface permite todas as operações necessárias

### **Qualidade do Código (25%)**
- ✅ Código bem estruturado e organizado
- ✅ Boas práticas de programação
- ✅ Separação adequada de responsabilidades
- ✅ Código legível e comentado quando necessário

### **Banco de Dados (20%)**
- ✅ Modelagem adequada das tabelas
- ✅ Consultas eficientes
- ✅ Integridade referencial
- ✅ Script de criação funcional

### **Interface do Usuário (10%)**
- ✅ Interface intuitiva e funcional
- ✅ Apresentação clara das informações
- ✅ Experiência do usuário satisfatória
- ✅ Responsividade básica

### **Documentação (5%)**
- ✅ README claro e completo
- ✅ Instruções de instalação funcionais
- ✅ Comentários no código quando necessário

---

## ⏰ **Informações de Prazo**

**Tempo Sugerido:** 3-5 dias úteis

**Entrega:** Código fonte completo + documentação via repositório Git ou arquivo compactado

---

## 🚀 **Dicas para Sucesso**

1. **Comece simples:** Implemente primeiro o cadastro de estoque
2. **Teste os cálculos:** Valide manualmente os cálculos do MRP
3. **Dados de exemplo:** Inclua dados de teste no script do banco
4. **Interface clara:** Priorize funcionalidade sobre design elaborado
5. **Documente bem:** README claro vale muito na avaliação

**Boa sorte com o desenvolvimento! 🛠️**