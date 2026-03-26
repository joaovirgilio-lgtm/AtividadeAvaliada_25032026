Avaliação Engenharia de Software.
sistema Integrado de Gestão de Farmácia MVP Definido pelo Estudante.

Aluno:João Pedro de Oliveira Virgilio
RA:25000110 
Data:25/03/2026

#1. Definição do MVP.
Meu MVP é sobre o processo de venda na farmacia como a consulta de produtos,cadastro do cliente,emissão do comprovante,verificação de estoque e registro de vendas
Dentro do MVP.
Realizar vendas
Consultar produtos
Verificar estoque
Cadastrar cliente
Emitir comprovante
Fora do MVP.
Gestão completa de fornecedores
Relatórios avançados
Controle administrativo completo
Transferência de uma unidade para outra
Justificativa.
Escolhido por ser o processo central do sistema.A venda integra cliente, produto e estoque,sendo o essencial para o funcionamneto da farmacia

#2. Regras de Negocio.
RN01 Toda venda deve atualizar automaticamente o estoque
RN02 Vendas a prazo geram automaticamente contas a pagar
RN03 Clientes devem estar cadastrados para comprar a prazo
RN04 O sistema deve emitir comprovante ao final da venda
RN05 Alertar quando um produto atingir o nível minimo de estoque

#3. Requisitos Funcionais.
RF01 Consultar produtos por nome ou codigo
RF02 Verificar se esta disponivel no estoque
RF03 Realizar venda de produtos
RF04 Permitir vendas a vista e a prazo
RF05 Cadastrar clientes
RF06 Emitir comprovante de venda
RF07 Registrar contas a pagar automaticamente
RF08 Atualizar estoque automaticamente após venda

#4. Requisitos Não Funcionais.
RNF01 O sistema deve responder em até 2 segundos
RNF02 O sistema deve possuir autenticação de usuarios
RNF03 Os dados devem ser armazenados com segurança
RNF04 O sistema deve estar disponível 24 horas todos os dias

#5. Casos de Uso.
Personagens:
Atendente
Farmaceutico
Cliente

#UC01 Realizar Vendas.
Ator:Atendente,cliente
Descrição:Permite ao atendente registrar a venda de produtos para um cliente
Pré-condições:Sistema ativo e produtos cadastrados
Pós-condições:Venda registrada e estoque atualizado
Fluxo Principal.

Atendente inicia a venda
Cliente solicita os produtos
Atendente consulta e seleciona produtos
Sistema verifica estoque
Sistema calcula venda
Atendente confirma venda
Sistema emite comprovante
Sistema atualiza estoque

Fluxos Alternativos.

FA01 Produto acabou sistema informa indisponibilidade 
FA02 Se o cliente não esta cadastrado dar uma opção de cadastro

<img width="323" height="921" alt="image" src="https://github.com/user-attachments/assets/0bb4f01e-38b5-4817-9830-6d628143fb16" />

#UC02 Consultar Produto.
Ator:Atendente,Farmacêutico
Descrição:Permite buscar informações de um produto
Pré-condições:Produto cadastrado no sistema
Pós-condições:Produto exibido

Fluxo Principal.

Farmaceutico informa nome ou código
Sistema busca produto
Sistema exibe informações
Atendente confiram o produto no estoque

Fluxos Alternativos.

FA01 Produto não encontrado.

<img width="319" height="312" alt="image" src="https://github.com/user-attachments/assets/2823ddd6-6587-448e-b330-9e2984b57014" />

#UC03 Verificar Estoque.
Ator:Atendente,Farmacêutico
Descrição:Verificar a quantidade disponível de um produto
Pré-condições:Produto cadastrado
Pós-condições:Quantidade exibida

Fluxo Principal.

Usuário seleciona produto
Sistema consulta estoque
Sistema exibe quantidade

Fluxos Alternativos.

FA01 Produto inexistente

<img width="248" height="312" alt="image" src="https://github.com/user-attachments/assets/7b905f13-74f9-4eee-af33-3aa5a5bd8d68" />

#UC04 Cadastrar Cliente.
Ator:Atendente
Descrição:Permite cadastrar um novo cliente
Pré-condições:Cliente não cadastrado
Pós-condições:Cliente salvo

Fluxo Principal.

Atendente coloca os dados
Sistema valida dados
Sistema salva cliente

Fluxos Alternativos.

FA01 Dados inválidos

<img width="232" height="312" alt="image" src="https://github.com/user-attachments/assets/6c6fd17a-a4e1-4a97-a669-17ae2e7b6380" />

UC05 Emitir Comprovante.
Ator:Sistema
Descrição:Gera comprovante da venda realizada
Pré-condições:Venda concluída
Pós-condições:Comprovante emitido

Fluxo Principal.

Sistema gera comprovante
Sistema exibe e imprime

Fluxos Alternativos.

FA01 Falha na impressão

<img width="262" height="257" alt="image" src="https://github.com/user-attachments/assets/be6883f1-242a-4158-8eed-fcbf05d5bf8f" />

#UC06 Gerar Conta a pagar.
Ator:Atendente
Descrição:Permite gerar uma cobrança futura ao cliente
Pré-condições:Venda a prazo
Pós-condições:Conta registrada

Fluxo Principal.

Atendente seleciona pagamento a prazo
Sistema gera conta
Sistema registra vencimento

Fluxos Alternativos

FA01 Cliente não pagou no prazo

<img width="311" height="312" alt="image" src="https://github.com/user-attachments/assets/a203f47e-2142-4cca-8035-55aac18440f3" />

#UC07 Validar Receita.
Ator:Farmacêutico
Descrição:Verifica a validade de receitas médicas
Pré-condições:Receita apresentada
Pós-condições:Receita validada ou recusada

Fluxo Principal.

Farmacêutico analisa receita
Sistema registra validação

Fluxos Alternativos.

FA01 Receita inválida

<img width="242" height="312" alt="image" src="https://github.com/user-attachments/assets/69679c13-ecbb-4403-a751-026a1c299a51" />

#UC08 Identificar Cliente.
Ator:Cliente
Descrição:Identifica cliente no sistema
Pré-condições:Cliente cadastrado
Pós-condições:Cliente identificado

Fluxo Principal.

Cliente informa dados
2Sistema localiza cliente
Sistema exibe dados

Fluxos Alternativos.

FA01 Cliente não encontrado

<img width="285" height="312" alt="image" src="https://github.com/user-attachments/assets/2b58334b-4f77-4e3d-87a2-d50f52323812" />

UC09 Calcular Total da Venda.
Ator:Sistema
Descrição:Calcula o valor total da compra
Pré-condições:Produtos selecionados
Pós-condições:Total calculado

Fluxo Principal.

Sistema soma valores
Aplica descontos
Exibe total

Fluxos Alternativos.

FA01 Erro de cálculo

<img width="227" height="312" alt="image" src="https://github.com/user-attachments/assets/450b87fb-9871-44df-8433-4d5cd8024e3c" />

#UC10 Cancelar Venda.
Ator:Atendente
Descrição:Permite cancelar uma venda realizada
Pré-condições:Venda existente
Pós-condições:Venda cancelada e estoque ajustado

Fluxo Principal.

Atendente seleciona venda
Sistema confirma ação
Sistema cancela venda
Sistema atualiza estoque

Fluxos Alternativos.

FA01 Venda já finalizada não tem como cancelar

<img width="356" height="367" alt="image" src="https://github.com/user-attachments/assets/a67c5aa8-7497-4709-8b35-217d5089af53" />
