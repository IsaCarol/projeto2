#.    Em execução 

# Análise de Vendas 2.0

Bem-vindo(a) ao meu projeto de Análise de Vendas

### 1º Passo - Banco de Dados

Para a criação do banco de dados, optei por utilizar o "PostgreSQL" juntamente com a ferramenta "DBeaver". 

### 2º Passo - Modelagem

Para dar início às modelagens, comecei pela modelagem de dados conceitual em um bloco de notas comum, onde escrevi em forma de tópicos o que seria necessário, pensando nos requisitos de negócios que gostaria de analisar e o que seria interessante visualizar.
Após fazer o modelo conceitual, utilizei o DrawSQL, uma plataforma online, para montar meu modelo lógico, montando a tabela fato e as dimensões, adicionando as métricas fundamentais em cada uma, fazendo todo relacionamento necessário entre as tabelas. 
Ao finalizar o modelo lógico, a plataforma "DrawSQL" permite fazer a exportação do arquivo para MySQL, PostegreSQL, etc, onde selecionei o suporte para PostgreSQL. Ao baixar o arquivo do modelo lógico, optei por executá-lo com o Visual Studio Code, pois lá já tenho a integração com meu banco de dados.
Dessa forma, o modelo físico já está pronto e foi só executar o script SQL dentro do VSCode e as tabelas foram adicionadas de forma automática ao meu banco de dados.
[Veja o Exemplo do Script SQL](Physical_Modeling)

### 3° Passo - Inserir Valores

O terceiro passo consistia em inserir os valores em cada uma das colunas das tabelas, e como queria fazer isso de forma automatizada, sem precisar inserir manualmente, pensei num scrip Python para realizar esta tarefa. Com a ajuda do ChatGPT, foi montado o script com todas as informações necessárias para inserir os valores fictícios em cada coluna das tabelas.
Nesse script foi adicionado as informações de conexão do meu banco de dados, então todos os insert's aconteceram de forma automática.
[Veja o Exemplo do Script Python](Script_Python_Insert)


### 4° Passo - Cálculos

Minha tabela FT_VENDAS ainda necessitava de uma coluna que mostrasse o valor total de vendas, então optei para realizar este passo antes de enviar meus dados para a ferramenta de visualização.
No DBeaver, criei um script SQL, fazendo uma alteração na minha tabela FT_VENDAS e adicionando a coluna VALOR_TOTAL, após realizar este passo, fiz um update na minha tabela FT_VENDAS adicionando os valores na coluna VALOR_TOTAL, fazendo um join, pois a minha quantidade vendida não estava na mesma tabela que a preço unitária.
[Veja o Script SQL](Add_Column)

### 5° Passo - Ferramenta de BI

Para realizar as análises de dados e a montagem do relatório, utilizei o Microsoft Power BI. Para importar meu conjunto de dados para a ferramenta, integrei diretamente ao meu banco de dados PostgreSQL, pois assim, qualquer modificação que for realizada no DB, será atualizada de forma automática no relatório de dados também. 
Carregado os dados, é hora de começar a análise.


### Requisitos de negócio

- Análise de Desempenho de Produtos
- Análise de Desempenho de Vendedores
- Análise Perfil do Cliente
- Análise de Canais de Venda
- Análise Temporal de Vendas


# Link dos arquivos

* Análise de Desempenho de Produtos
[Análise Desempenho dos Produtos](analiseproduto.png)

* Análise Temporal de Vendas
[Análise Desempenho Tempo](analisetempo.png)

* Análise de Desempenho de Vendedores
[Análise Desempenho dos Vendedores](https://github.com/IsaCarol/projeto2/blob/main/analisevendedor%20.png)

* Análise Perfil do Cliente
[Análise Perfil Cliente](analisecliente.png)


[Veja o vídeo do projeto]([https://drive.google.com/file/d/1A2B3C4D5E6F7G8H9/view?usp=sharing](https://drive.google.com/drive/folders/1jjD3sXFUctN7KVr8DHfr8tYDQ9-xwqJ1?usp=sharing)



### Links Úteis

DrawSQL: https://drawsql.app/

