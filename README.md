# Projeto de Banco de Dados

Bem-vindo ao repositório do **Projeto de Banco de Dados**! 🚀 Este projeto abrange três fases principais no design de um banco de dados, com o objetivo de criar um modelo robusto e eficiente para diferentes cenários. Abaixo, você encontrará detalhes sobre as fases do projeto e as entidades envolvidas.

## 🛠️ Fases do Projeto

1. **Levantamento de Requisitos**
2. **Projeto Conceitual: Modelo ER**
3. **Projeto Lógico: Modelo Relacional**

## 🌟 Entidades e Cenários

### 1. Ordem de Serviço

**Contexto:** Em uma empresa, clientes solicitam ações ao help desk, convertidas em Ordens de Serviço (OS) com tempo associado.

**Entidades Mapeadas:**
- **Cliente**
- **Responsável**
- **Pedido**
- **Ordem de Serviço**

**Relacionamentos:**
- Solicita
- Analisa
- Executa
- Arquiva

**Narrativa:** O cliente realiza um pedido que é convertido em OS, sendo analisado e executado por um técnico. Se necessário, a OS é cancelada e arquivada após a execução.

### 2. Universidade

**Contexto:** Foco no ensino e gestão de alunos e cursos.

**Entidades:**
- **Professor**
- **Curso**
- **Coordenação**
- **Disciplina**
- **Aluno**

**Narrativas:**
- **Alunos:** Alunos podem estar matriculados em vários cursos e realizar cursos complementares. Eles são avaliados por provas e trabalhos.
- **Disciplinas:** Oferecidas por um professor, podem ter pré-requisitos e serem comuns a diferentes cursos. O ciclo de vida das disciplinas é semestral.
- **Professores:** Associados às coordenações de seus cursos.

**Perguntas para o Cliente:**
- Quais informações sobre alunos e professores devem ser armazenadas?
- Qual a média para aprovação?
- Haverá restrições ou diferentes visões?

### 3. Ecommerce

**Contexto:** Objetivo é a venda de produtos. O sistema deve suportar operações de compra, estoque e gerenciamento de pedidos.

**Entidades e Atributos:**
1. **Produto**
   - ID_Produto (PK)
   - Nome
   - Descrição
   - Preço
   - Quantidade_Estoque
   - ID_Fornecedor (FK)
   
2. **Fornecedor**
   - ID_Fornecedor (PK)
   - Nome
   - CNPJ (ou CPF)
   - Endereço
   
3. **Cliente**
   - ID_Cliente (PK)
   - Nome
   - CPF (ou CNPJ)
   - Endereço
   - Telefone
   - Email
   
4. **Pedido**
   - ID_Pedido (PK)
   - ID_Cliente (FK)
   - Data_Pedido
   - Data_Envio (opcional)
   - Data_Cancelamento (opcional)
   - Valor_Total
   - Endereço_Entrega (opcional)
   - Status (ex: Pendente, Enviado, Cancelado)
   
5. **Item_Pedido**
   - ID_Item_Pedido (PK)
   - ID_Pedido (FK)
   - ID_Produto (FK)
   - Quantidade
   - Preço_Unitario

**Relacionamentos:**
- **Produto - Fornecedor:** Um produto é fornecido por um único fornecedor.
- **Pedido - Cliente:** Um pedido é feito por um único cliente.
- **Pedido - Item_Pedido:** Um pedido pode ter vários itens.
- **Produto - Item_Pedido:** Cada item no pedido refere-se a um produto específico.

**Observações:**
- **Estoque:** A quantidade em estoque pode ser um atributo do produto ou uma entidade separada.
- **Cancelamento de Pedidos:** Pode ser necessário adicionar atributos e regras específicas.
- **Endereço de Entrega:** Opcional, pode ser modelado como uma entidade separada se necessário.

## 🔧 Ferramenta Utilizada

Utilize o **MySQL Workbench** para criar e visualizar o Diagrama Entidade-Relacionamento (DER). Certifique-se de definir corretamente as chaves primárias e estrangeiras e garantir que os relacionamentos estejam bem representados.

---

## Contribuições

Sinta-se à vontade para contribuir com melhorias ou sugestões. Para isso, crie um fork deste repositório e envie um pull request com suas alterações.

## Contato

Para qualquer dúvida ou sugestão, entre em contato pelo [vitorbeatle@gmail.com].

---

Esperamos que este projeto seja útil e inspirador para suas práticas de modelagem de banco de dados. Divirta-se explorando e refinando!

---
