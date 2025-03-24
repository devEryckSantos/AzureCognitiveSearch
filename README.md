# Passo a Passo para se Configurar uma Pesquisa
Para utilizar o Azure AI Search para realizar uma pesquisa, é preciso seguir alguns passos:  
[Documentação necessária](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

## Passo 1: Criando um Recurso Azure AI Search
Vá até o portal do Azure, clique em "Criar um recurso" e pesquise pela ferramenta "Azure AI Search". Selecione a ferramenta e preencha os campos necessários para cria-lá.  

## Passo 2: Criando um Recurso de IA
Agora precisaremos criar um serviço de IA. Seguindo o mesmo passo anterior, clique em "Criar um recurso", selecione a categoria "IA + Machine Learning" e busque por "Azure AI services". Assim, poderemos criar um novo recurso de Inteligência Artificial.

## Passo 3: Criando uma Conta de Armazenamento
Nosso terceiro e último recurso. Novamente, clique em "Criar um recurso" e busque por "Storage Accounts". Clique em "create" e preencha apenas os campos presentes na aba "Basics". No campo "Redudancy", selecione a opção "Locally-redudant storage (LRS)". Após preencher as informações, clique em "Review + create".  

## Passo 4: Quebrando as Regras de Segurança do Storage Account
Por padrão, o Storage Account vem com algumas regras de segurança que, para o nosso laboratório, precisaremos quebrar. A primeira coisa que precisamos fazer, é ir em "Settings" colocar o "Allow Blob anonymous access" como **enable** e clique em "Save".  
Após isso, vá até "Data Storag" e clique em "Containers" para que possamos trazer alguns arquivos dentro do nosso container.

## Passo 5: Adicionando Arquivos no Container
Dentro do container, clique em "+ Container" e mude o "Anonymous access level" para "Container(...)" e o nomeie como "coffeereviews". Entre em seu container recém criado e façao "upload" dos arquivos **"zipped coffee reviews"** disponíveis na documentação.  
Seguindo esses 5 passos, já temos criado um **mecanismo de busca**, um **recurso de IA** e um **Storage Account** com algumas informações.

## Passo 6: Importando dados
Agora, para finalizarmos, devemos ir até o nosso mecanismo de busca e clicar em "import data". Selecione o Azure Blob Storage e preencha os detalhes do armazenamento de dados com os seguintes valores:  
Fonte de dados : Armazenamento de Blobs do Azure.  
Nome da fonte de dados : coffee-customer-data.  
Dados a extrair : Conteúdo e metadados.  
Modo de análise : Padrão.  
String de conexão : *Selecione Choose an existing connection . Selecione sua conta de armazenamento, selecione o contêiner coffee-reviews e clique em Select.  
Autenticação de identidade gerenciada : Nenhuma.  
Nome do contêiner : esta configuração é preenchida automaticamente depois que você escolhe uma conexão existente.  
Pasta Blob : deixe em branco.  
Descrição : Avaliações das cafeterias Fourth Coffee.  

Por fim, selecione: Next: Add cognitive skills (Optional).

## Passo 7: Contultando Index
Use o "Search explorer" para escrever e testar consultas e revisar resultados em JSON. Abaixo do índice selecionado, altere a visualização para **JSON view** e no campo "JSON query editor", faça suas perquisas no formato JSON, por exemplo:  
{"search": "*", "count": true}  
Selecione Search e a consulta de pesquisa retornará todos os documentos no índice de pesquisa.
