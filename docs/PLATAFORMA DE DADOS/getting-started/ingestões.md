---
title: Ingestões
deprecated: false
hidden: false
metadata:
  robots: index
---
Nesta seção, explicamos o passo a passo para fazer:

* fazer ingestões completas (carga full);
* fazer ingestões incrementais (carga incremental);
* fazer uploads de planilhas;
* visualizar ingestões realizadas com sucessos e ocorrências de erros.

# Nova ingestão

A ingestão é  o processo de buscar um dado na origem e disponibilizá-lo na Data Platform.

## Como realizar uma ingestão completa de dados (carga full)

1. Acesse a opção “Nova ingestão” pelo menu da Data Platform.

2. <br />

3. Selecione uma das Conexões disponíveis. A Conexão é a origem (ou a fonte) dos dados.

<br />

1. Digite, no campo correspondente, o nome da Tabela que se deseja fazer a ingestão.

2. Utilize o campo Hash em colunas, caso seja necessário ocultar os dados sensíveis. Basta digitar o nome da coluna que precisa ser ocultada na ingestão.  Se for necessário proteger informações de mais de uma coluna, separe os nomes das colunas por vírgulas. Este é uma opção que criptografa os dados nas colunas informadas utilizando algoritmos de Hash, o que impede a recuperação do dado original.

3. Habilite o botão Ativo para que a ingestão seja feita de forma automática. Dessa forma, a ingestão cadastrada será realizada todos os dias, no horário de 1h da manhã.

4. Conclua o cadastro da ingestão clicando no botão Salvar. Se todas as informações estiverem corretas, a ingestão será processada no próximo horário programado.

Como realizar uma ingestão incremental de dados (carga incremental)

1. Repita os passos de 1 a 5 do item Como realizar uma ingestão completa de dados (carga full).

2. Informe o campo Coluna Controle. Informe uma coluna da tabela que mostre a data e hora em que cada registro foi incluído ou alterado.

3. Informe o campo Coluna Identificadora. Informe uma ou mais colunas que identificam cada registro de forma única (chave primária ou unique key). Essas colunas ajudam a evitar dados duplicados, mantendo sempre o registro mais atualizado.

4. Clique no botão Salvar.Como realizar uma ingestão incremental de dados (carga incremental) com template de incremento
   Você pode utilizar o campo Template para definir uma regra de incremento personalizada para a tabela. Isso é útil, por exemplo, quando a tabela tem duas ou mais colunas que devem ser combinadas. Para definir uma ingestão incremental com template de incremento, basta seguir os passos abaixo:

5. Repita os passos de 1 a 3 do item Como realizar uma ingestão incremental de dados (carga incremental).

6. Informe o campo Template.

7. Você pode encontrar instruções detalhadas de como criar um template clicando no ícone de informação.

8. Clique no botão Salvar.Informações importantes
   As informações “Conexão” e “Tabela” são obrigatórias para o processo de ingestão.
   É possível salvar a ingestão cadastrada ainda que o nome da Tabela esteja incorreto. No entanto, ocorrerá um erro no processo de ingestão, já que a Tabela não será localizada.
   O “Hash em colunas” é opcional. Utilize essa função para proteger dados sensíveis.
   Ao preencher o campo Coluna controle é preciso preencher também o campo Coluna identificadora!
   Ao preencher o campo Coluna identificadora é preciso preencher também o campo Coluna controle!
   Ao preencher o campo Template é preciso preencher também Coluna controle e Coluna identificadora!
   Você não poderá incluir uma tabela já cadastrada.
   A ingestão não é feita automaticamente ao clicar no botão “Salvar”. Todas as ingestões são processadas diariamente, 1h da manhã.

Listar ingestõesPara listar as ingestões cadastradas, basta selecionar a opção Listar Ingestões no menu principal.

O ícone  permite que você altere os dados de uma ingestão já cadastrada, basta clicar no ícone.O ícone  permite que você visualize os detalhes (logs) da última execução do processo de ingestão, basta clicar no ícone.
A coluna status informa a situação da ingestão:
indica que a última execução da ingestão foi executada com sucesso.
indica que ocorreu um erro ao executar a ingestão da tabela.
indica que algum alerta foi disparado durante o processo.
Os detalhes de erros e alertas podem ser vistos ao clicar no ícone .
A coluna Ativo informa se a ingestão está ativa ou não:
A ingestão está ativa.
A ingestão não está ativa.

Alterar ingestãoPara editar uma ingestão, basta selecionar a opção Listar Ingestões no menu principal e, em seguida, clicar no ícone  referente à ingestão desejada.

Você será direcionado para a tela de alteração com os campos da ingestão carregados.

Visualizar Logs da ingestãoPara visualizar os logs de uma ingestão, basta selecionar a opção Listar Ingestões no menu principal e, em seguida, clicar no ícone  referente à ingestão desejada.

Um popup será exibido com os detalhes (logs) da última execução do processo de ingestão, conforme abaixo:

Iniciar o processo de ingestão manualmenteSe você não puder esperar até o dia seguinte para visualizar os dados da sua tabela, você pode iniciar o processo de ingestão manualmente. Para isso, basta selecionar a opção Listar Ingestões no menu principal, selecionar a sua tabela na lista de ingestões (uma ou mais) e clicar em "Processar”.

Após confirmar o início do processo, basta aguardar a finalização.Informações importantes
Ao iniciar o processo de ingestão manualmente, você deverá aguardar a finalização do procedimento para iniciar outra execução.
Você precisa selecionar ao menos uma tabela para iniciar o processo.
Tabelas que não estão ativas NÃO podem ser selecionadas para ingestão manual.
Existe um número máximo de vezes que um usuário pode iniciar o processo manualmente. Atualmente, este limite está definido em duas execuções diárias.