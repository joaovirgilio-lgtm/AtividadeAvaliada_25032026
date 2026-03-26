**Avaliação Engenharia de Software**
**Sistema Integrado de Gestão de Farmácia – MVP Definido pelo Estudante**

**Aluno:** João Pedro de Oliveira Virgilio
**RA:** 25000110
**Data:** 25/03/2026

---

## #1. Definição do MVP

Meu MVP é sobre o processo de venda na farmácia, incluindo consulta de produtos, cadastro de cliente, emissão de comprovante, verificação de estoque e registro de vendas.

### Dentro do MVP:

* Realizar vendas
* Consultar produtos
* Verificar estoque
* Cadastrar cliente
* Emitir comprovante

### Fora do MVP:

* Gestão completa de fornecedores
* Relatórios avançados
* Controle administrativo completo
* Transferência entre unidades

### Justificativa:

Escolhido por ser o processo central do sistema. A venda integra cliente, produto e estoque, sendo essencial para o funcionamento da farmácia.

---

## #2. Regras de Negócio

RN01 – Toda venda deve atualizar automaticamente o estoque
RN02 – Vendas a prazo geram automaticamente contas a receber
RN03 – Clientes devem estar cadastrados para comprar a prazo
RN04 – O sistema deve emitir comprovante ao final da venda
RN05 – Alertar quando um produto atingir o nível mínimo de estoque

---

## #3. Requisitos Funcionais

RF01 – Consultar produtos por nome ou código
RF02 – Verificar se está disponível no estoque
RF03 – Realizar venda de produtos
RF04 – Permitir vendas à vista e a prazo
RF05 – Cadastrar clientes
RF06 – Emitir comprovante de venda
RF07 – Registrar contas a receber automaticamente
RF08 – Atualizar estoque automaticamente após venda

---

## #4. Requisitos Não Funcionais

RNF01 – O sistema deve responder em até 2 segundos
RNF02 – O sistema deve possuir autenticação de usuários
RNF03 – Os dados devem ser armazenados com segurança
RNF04 – O sistema deve estar disponível 24 horas por dia

---

## #5. Casos de Uso

### Personagens:

* Atendente
* Farmacêutico
* Cliente

---

## #UC01 – Realizar Vendas

**Atores:** Atendente, Cliente

**Descrição:** Permite ao atendente registrar a venda de produtos para um cliente.

**Pré-condições:** Sistema ativo e produtos cadastrados
**Pós-condições:** Venda registrada e estoque atualizado

### Fluxo Principal:

1. Atendente inicia a venda
2. Cliente solicita os produtos
3. Atendente consulta e seleciona produtos
4. Sistema verifica estoque
5. Sistema calcula venda
6. Atendente confirma venda
7. Sistema emite comprovante
8. Sistema atualiza estoque

### Fluxos Alternativos:

FA01 – Produto indisponível: sistema informa falta
FA02 – Cliente não cadastrado: sistema oferece opção de cadastro

---

## #UC02 – Consultar Produto

**Atores:** Atendente, Farmacêutico

**Descrição:** Permite buscar informações de um produto

**Pré-condições:** Produto cadastrado
**Pós-condições:** Produto exibido

### Fluxo Principal:

1. Farmacêutico informa nome ou código
2. Sistema busca produto
3. Sistema exibe informações
4. Atendente confere o produto no estoque

### Fluxo Alternativo:

FA01 – Produto não encontrado

---

## #UC03 – Verificar Estoque

**Atores:** Atendente, Farmacêutico

**Descrição:** Verifica a quantidade disponível de um produto

**Pré-condições:** Produto cadastrado
**Pós-condições:** Quantidade exibida

### Fluxo Principal:

1. Usuário seleciona produto
2. Sistema consulta estoque
3. Sistema exibe quantidade

### Fluxo Alternativo:

FA01 – Produto inexistente

---

## #UC04 – Cadastrar Cliente

**Ator:** Atendente

**Descrição:** Permite cadastrar um novo cliente

**Pré-condições:** Cliente não cadastrado
**Pós-condições:** Cliente salvo

### Fluxo Principal:

1. Atendente insere os dados
2. Sistema valida dados
3. Sistema salva cliente

### Fluxo Alternativo:

FA01 – Dados inválidos

---

## #UC05 – Emitir Comprovante

**Ator:** Sistema

**Descrição:** Gera comprovante da venda realizada

**Pré-condições:** Venda concluída
**Pós-condições:** Comprovante emitido

### Fluxo Principal:

1. Sistema gera comprovante
2. Sistema exibe e imprime

### Fluxo Alternativo:

FA01 – Falha na impressão

---

## #UC06 – Gerar Conta a Receber

**Ator:** Atendente

**Descrição:** Permite gerar uma cobrança futura ao cliente

**Pré-condições:** Venda a prazo
**Pós-condições:** Conta registrada

### Fluxo Principal:

1. Atendente seleciona pagamento a prazo
2. Sistema gera conta
3. Sistema registra vencimento

### Fluxo Alternativo:

FA01 – Cliente não paga no prazo

---

## #UC07 – Validar Receita

**Ator:** Farmacêutico

**Descrição:** Verifica a validade de receitas médicas

**Pré-condições:** Receita apresentada
**Pós-condições:** Receita validada ou recusada

### Fluxo Principal:

1. Farmacêutico analisa receita
2. Sistema registra validação

### Fluxo Alternativo:

FA01 – Receita inválida

---

## #UC08 – Identificar Cliente

**Ator:** Cliente

**Descrição:** Identifica cliente no sistema

**Pré-condições:** Cliente cadastrado
**Pós-condições:** Cliente identificado

### Fluxo Principal:

1. Cliente informa dados
2. Sistema localiza cliente
3. Sistema exibe dados

### Fluxo Alternativo:

FA01 – Cliente não encontrado

---

## #UC09 – Calcular Total da Venda

**Ator:** Sistema

**Descrição:** Calcula o valor total da compra

**Pré-condições:** Produtos selecionados
**Pós-condições:** Total calculado

### Fluxo Principal:

1. Sistema soma valores
2. Aplica descontos
3. Exibe total

### Fluxo Alternativo:

FA01 – Erro de cálculo

---

## #UC10 – Cancelar Venda

**Ator:** Atendente

**Descrição:** Permite cancelar uma venda realizada

**Pré-condições:** Venda existente
**Pós-condições:** Venda cancelada e estoque ajustado

### Fluxo Principal:

1. Atendente seleciona venda
2. Sistema confirma ação
3. Sistema cancela venda
4. Sistema atualiza estoque

### Fluxo Alternativo:

FA01 – Venda já finalizada só pode ser cancelada com autorização
