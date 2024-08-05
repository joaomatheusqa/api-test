## Teste da API ServeRest com Postman

**Introdução**
Bem-vindo ao repositório do meu primeiro projeto de testes de API! Este projeto utiliza o Postman para testar a API ServeRest, cobrindo tanto cenários positivos quanto negativos. O objetivo é garantir que a API esteja funcionando conforme esperado em diferentes situações.

**Estrutura do Projeto**
O projeto está organizado em duas categorias principais de testes:

**Cenários Positivos**: Verifica se a API responde corretamente aos casos de uso esperados.
**Cenários Negativos**: Testa a API com dados que devem gerar erros para validar o comportamento da API em situações não ideais.


**Cenários Positivos**

**Listar Usuários**
Descrição: Testa a listagem de usuários.
Verificações: Confirma que a resposta tem o status 200 e que a lista de usuários está presente e é um array.


**Criar Usuário**
Descrição: Testa a criação de um novo usuário.
Verificações: Verifica se o status é 201 e se a mensagem de sucesso está presente. Salva o ID do usuário criado em uma variável de ambiente para uso posterior.


**Buscar Usuário por ID**
Descrição: Testa a busca de um usuário usando o ID.
Verificações: Confirma que a resposta tem o status 200 e que o ID retornado corresponde ao ID usado na solicitação. Também verifica a presença de outros campos esperados.


**Editar um Usuário**
Descrição: Testa a atualização de um usuário existente.
Verificações: Verifica se o status é 200 e se a resposta contém a mensagem de sucesso.


**Deletar um Usuário**
Descrição: Testa a exclusão de um usuário.
Verificações: Confirma que a resposta contém a mensagem de sucesso indicando que o registro foi excluído.


**Cenários Negativos**

**Criar Usuário com Dados Existentes**
Descrição: Testa a criação de um usuário com um e-mail já existente.
Verificações: Verifica se a resposta tem o status 400 e se a mensagem de erro correspondente é retornada.


**Buscar Usuário com ID Inválido**
Descrição: Testa a busca por um usuário usando um ID inválido.
Verificações: Confirma que a resposta tem o status 400 e contém a mensagem de erro apropriada.


**Funções Utilizadas**
Variáveis de Ambiente e Globais: Utilizadas para armazenar e reutilizar dados, como IDs de usuários e informações aleatórias geradas durante os testes.
Scripts de Prerequest: Geram dados aleatórios e configuram variáveis antes da execução das requisições.
Scripts de Teste: Validam a resposta das requisições, checando status codes, mensagens e outros campos específicos.


**Como Executar os Testes**

Clone o Repositório
git clone https://github.com/seu-usuario/teste-api-servrest.git

Importe a Coleção no Postman
Abra o Postman e importe a coleção de testes.
Configure as Variáveis de Ambiente

Defina as variáveis de ambiente necessárias, como a URL base da API.

**Execute os Testes**
Execute os testes no Postman ou use o Newman para rodar a coleção via linha de comando:
newman run Teste_ServeRest_Usuario.json -e variaveis

**Conclusão**
Este projeto demonstra a capacidade de testar APIs de forma estruturada e abrangente utilizando o Postman. Através de cenários positivos e negativos, garantimos que a API ServeRest esteja robusta e pronta para produção.
