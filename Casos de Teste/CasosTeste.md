**Projeto de Teste SWAG - Documento de Teste**

*Detalhes do Projeto*

- **ID do Projeto:** 10001
- **Chave do Projeto:** SWAG

*Planos de Teste*

**Chave:** SWAG-P1
- **Nome:** Testes funcionais
- **Descrição:** ​​​​​Testes da Sprint 1
- **Ciclos inclusos**: SWAG-R1 e SWAG-R2

*Ciclos de Teste*

1 - **Chave:** SWAG-R1
- **Nome:** Ciclo de teste para confirmação de cadastro.
- **Descrição:** Verificar se todo ciclo de cadastro e confirmação esta funcionando corretamente.
- **Testes de casos inclusos**: SWAG-T5, SWAG-T6 e SWAG-T7

2 - **Chave:** SWAG-R2
- **Nome:** Ciclo de teste para função acrescentar mais itens de um mesmo produto ao carrinho.
- **Descrição:** Testes da função acrescentar mais itens de um mesmo produto ao carrinho
- **Testes de casos inclusos**: SWAG-T2, SWAG-T3 e SWAG-T4

*Testes*
1. **SWAG-T2 - Adicionar Mais de Uma Unidade do Mesmo Item no Carrinho**
   - **Criado por:** Alan Torres
   - **Data de Criação:** 11 de novembro de 2023, 20:49:13 UTC
   - **Objetivo:** Garantir que o usuário possa adicionar mais de uma unidade do mesmo item ao carrinho.
   - **Pré-condição:** O usuário está logado na loja virtual.
   - **Status:** Em Progresso
   - **Script de Teste: BDD**
     ```
     Given que o usuário está logado na loja virtual
     When o usuário seleciona um item e adiciona mais de uma unidade ao carrinho
     Then a quantidade de unidades do item no carrinho deve ser igual à quantidade desejada
     And o total do carrinho deve ser recalculado corretamente
     ```

2. **SWAG-T3 - Atualização da Quantidade no Carrinho**
   - **Criado por:** Alan Torres
   - **Data de Criação:** 11 de novembro de 2023, 20:50:18 UTC
   - **Objetivo:** Verificar se o total do carrinho é recalculado corretamente após o ajuste da quantidade de um item.
   - **Pré-condição:** O usuário possui itens no carrinho.
   - **Status:** Em Progresso
   - **Script de Teste: BDD**
     ```
     Given que o usuário possui itens no carrinho
     When o usuário acessa o carrinho e ajusta a quantidade de um item específico
     And confirma as alterações
     Then o total do carrinho deve ser recalculado corretamente
     ```

3. **SWAG-T4 - Limite de Estoque**
   - **Criado por:** Alan Torres
   - **Data de Criação:** 11 de novembro de 2023, 20:51:29 UTC
   - **Objetivo:** Verificar se o sistema lida corretamente com tentativas de adicionar ao carrinho quando a quantidade desejada não está disponível.
   - **Pré-condição:** O item selecionado tem uma quantidade disponível em estoque menor que a desejada pelo usuário.
   - **Status:** Em Progresso
   - **Script de Teste: BDD**
     ```
     Given que o item selecionado tem uma quantidade disponível em estoque menor que a desejada pelo usuário
     When o usuário tenta adicionar uma quantidade maior do que a disponível em estoque ao carrinho
     Then uma mensagem de erro deve ser exibida informando que a quantidade desejada não está disponível
     And o carrinho não deve ser atualizado com quantidades além do estoque disponível
     ```

4. **SWAG-T5 - Verificar E-mail de Confirmação Após o Cadastro**
   - **Criado por:** Alan Torres
   - **Data de Criação:** 11 de novembro de 2023, 20:54:47 UTC
   - **Objetivo:** Garantir que o cliente receba um e-mail de confirmação após o cadastro bem-sucedido.
   - **Pré-condição:** O usuário recém-cadastrado inseriu informações válidas durante o processo de registro.
   - **Status:** Em Progresso
   - **Script de Teste: step-by-step**
     ```
     Passo 1: Um usuário completa o processo de cadastro na loja virtual.
     Dados Teste: O cadastro é bem-sucedido.
     Resultado Esperado: Informações válidas do usuário.

     Passo 2: O sistema envia um e-mail de confirmação.
     Dados Teste: -
     Resultado Esperado: Um e-mail de confirmação é enviado para o usuário.

     Passo 3: O cliente verifica imediatamente e recebe com sucesso o e-mail de confirmação.
     Dados Teste: O e-mail de confirmação é recebido com sucesso.
     Resultado Esperado: Caixa de entrada de e-mail.

     Passo 4: O e-mail de confirmação contém as informações relevantes.
     Dados Teste: O e-mail contém informações sobre a confirmação.
     Resultado Esperado: Conteúdo do e-mail de confirmação.
     ```

5. **SWAG-T6 - Confirmação Bem-Sucedida na Tela de Confirmação**
   - **Criado por:** Alan Torres
   - **Data de Criação:** 11 de novembro de 2023, 20:56:03 UTC
   - **Objetivo:** Garantir que a confirmação é bem-sucedida ao seguir os passos indicados na tela.
   - **Pré-condição:** O cliente acessou a tela de confirmação.
   - **Status:** Em Progresso
   - **Script de Teste: step-by-step**
     ```
     Passo 1: Um cliente abre o e-mail de confirmação.
     Dados Teste: O e-mail de confirmação está disponível.
     Resultado Esperado: Caixa de entrada de e-mail.

     Passo 2: O e-mail de confirmação foi recebido com sucesso.
     Dados Teste: -
     Resultado Esperado: O e-mail de confirmação está disponível para leitura.

     Passo 3: O cliente clica no link fornecido no e-mail.
     Dados Teste: Cliente é redirecionado para a tela de confirmação.
     Resultado Esperado: Link no e-mail de confirmação.

     Passo 4: O cliente é redirecionado para a tela de confirmação.
     Dados Teste: O cliente está na tela de confirmação.
     Resultado Esperado: Tela de confirmação.
     ```

6. **SWAG-T7 - Conteúdo do E-mail de Confirmação**

    - **Criado por:** Alan Torres
    - **Data de Criação:** 11 de novembro de 2023, 20:57:49 UTC
    - **Objetivo:** Verificar se o e-mail de confirmação contém informações relevantes sobre a confirmação.
    - **Pré-condição:** O usuário recém-cadastrado inseriu informações válidas durante o processo de registro.
    - **Status:** Em Progresso
    - **Script de Teste: step-by-step**
    ```
    Passo 1: Um usuário completa o processo de cadastro na loja virtual.
    Dados Teste: O cadastro é bem-sucedido.
    Resultado Esperado: Informações válidas do usuário.

    Passo 2: O sistema envia o e-mail de confirmação.
    Dados Teste: -
    Resultado Esperado: Um e-mail de confirmação é enviado para o usuário.

    Passo 3: O e-mail de confirmação é verificado.
    Dados Teste: O e-mail de confirmação é recebido com sucesso.
    Resultado Esperado: Caixa de entrada de e-mail.

    Passo 4: O e-mail de confirmação contém informações relevantes sobre a confirmação.
    Dados Teste: O e-mail contém informações sobre a confirmação.
    Resultado Esperado: Conteúdo do e-mail de confirmação.
    ```
