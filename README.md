# Construindo API's robustas utilizando Python
Tutorial 16 da Python Brasil 2021 <br>
Ministrante: Luizalabs (facilitador: Cassio Botaro)


Neste tutorial vamos aprender a construir API's utilizando Python e FastAPI, integrá-las a serviços externos e também a como torná-las robustas. Discutiremos a importância de uma boa documentação e testes.

Abordaremos conceitos como integração com serviços externos, integração contínua e testes automatizados. Analisaremos cenários onde precisaremos de uma melhor performance e algumas técnicas para alcançar este objetivo como chamadas a funções assíncronas.

Vamos tentar nos preparar para situações ruins que possam acontecer e garantir que nosso sistema será resiliente.

### Tópicos abordados

- Integração com serviços externos
- Integração contínua
- Testes automatizados
- Invocação de processos assíncronos
- Circuit breaker
- Compartilhamento de memória

### O que será desenvolvido?
Será desenvolvido um sistema com objetivo de obter informações a respeito de pedidos.

Os pedidos serão obtidos através de integração com o sistema de pedidos do Magalu.

Vamos fazer o enriquecimento desta informação antes de sua exibição e também iremos prover alguns dados estatísticos sobre o pedido.

Um pedido possui vários pacotes, cada um deles contendo itens.

Este sistema deve seguir as seguintes regras:<br>
- Deve apresentar uma interface que possa ser consumida tanto por um website, quanto por um aplicativo para dispositivos móveis;<br>
- Deve prover um endpoint que indique a saúde do sistema;<br>
- Dado um pedido, retornar os seus itens;<br>
- Os itens de um pedido devem conter um identificador (sku), uma descrição, uma imagem, uma referência e a quantidade;<br>
- Exibir um relatório com o total de métodos de pagamento utilizados nos últimos 30 pedidos;<br>
- Dado um pedido (vários itens), enriquecer a informação com as informações de gtin (global trade item number). Deve ser retornado também a marca, descrição e - identificação do produto;<br>
- Como será consumido por terceiros deve apresentar boa documentação;<br>
- O sistema deve estar preparado para receber novas funcionalidades, garantindo qualidade a cada entrega;<br>
- O sistema deve apresentar testes.<br>


### Ferramentas
```bash
Python
FastApi
Poetry
```

### Para testa, basta roda o comando:

```bash
uvicorn --reload api_pedidos.api:app.
```