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




