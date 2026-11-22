# Exceções: Conta Bancária

Exercício de fixação em Java sobre tratamento de exceções.

## O que o programa faz

Lê os dados de uma conta bancária (número, titular, saldo inicial e limite de saque) e realiza um saque, mostrando o novo saldo. O saque é recusado quando:

- o valor é maior que o limite de saque da conta;
- o valor é maior que o saldo disponível.

Nesses casos, o programa mostra uma mensagem de erro em vez de quebrar.

## Tecnologias

- Java
- Eclipse IDE

## Estrutura do projeto

- `application`: classe `Program`, que lê os dados e trata os erros
- `model.entities`: classe `Account`, com os métodos `deposit` e `withdraw`
- `model.exceptions`: classe `DomainException`, exceção criada para as regras da conta

## Exemplo de execução

Saque válido:

    Enter account data
    Number: 8840
    Holder: Alex Oliveira
    Initial balance: 500.00
    Withdraw limit: 300.00

    Enter amount for withdraw: 100.00
    New balance: 400.00

Saque acima do limite:

    Enter amount for withdraw: 400.00
    Withdraw error: The amount exceeds withdraw limit

## O que aprendi

- Criar uma exceção própria (`DomainException`)
- Lançar exceções com `throw` dentro da classe, para que a regra de negócio fique na `Account` e não no `Program`
- Tratar erros com `try/catch` e mostrar a mensagem com `getMessage()`
- Formatar números com `printf` e `%.2f`
