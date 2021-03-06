# INF1629-PES

WtranS - Workshop de Transparência em Sistemas

Esse projeto pertence à disciplina "INF1629 - Princípios de Engenharia de Software" da PUC-RIO.

Alunas desenvolvedoras: Ingrid Coda, Mariela Andrade e Pilar Fernandez.

Baseado no [WtranS](http://wtrans.inf.puc-rio.br), este projeto tem o objetivo de listar artigos acadêmicos. 
Nosso diferencial do projeto original é a fonte de consumo dos dados que alimentam o site. 
Nosso intuito é transformar o conteúdo do banco de dados MySQL usado no projeto original em arquivos .JSON e adaptar o código fonte do projeto para consumir os dados dessa nova fonte. 

URL de acesso: [http://wtransdev.inf.puc-rio.br](http://wtransdev.inf.puc-rio.br)

Segue abaixo a documentação do projeto:

  1) Linguagem de Definição:

  - Cenário 1:
    - Título:	Migração do banco de dados do WtranS.
    - Objetivo:	Migrar banco de SQL para JSON.
    - Contexto:	Banco de dados SQL.
    - Atores:	Desenvolvedores.
    - Recursos:	Banco de dados SQL.
    - Episódio: Fazer a migração do banco em SQL para JSON usando um comando do MySQL.
    - Restrição: Não alterar valores das tabelas.
    - Exceção: Trancamento da disciplina, problemas na interpretação do trabalho, problemas de saúde com os desenvolvedores.

  - Cenário 2:
    - Título:	Integração do WtranS com JSON
    - Objetivo:	Aplicação WtranS consumir dados advindos dos arquivos JSON.
    - Contexto:	Sistema de busca de artigos acadêmicos e arquivos JSON com dados desses artigos.
    - Atores:	Desenvolvedores.
    - Recursos:	Código fonte do projeto escrito em LUA e arquivos JSON.
    - Episódio: Alterar os arquivos do WtranS, principalmente o papers_by_conference.lp e o index.lp, para que eles leiam os dados da                     nova fonte (JSON) e não mais do banco de dados SQL. 
    - Restrição: Não causar perda de performance do sistema.
    - Exceção: Trancamento da disciplina, problemas na interpretação do trabalho, problemas de saúde com os desenvolvedores.

  - Cenário 3:
    - Título:	Geração do arquivo XML no padrão solicitado.
    - Objetivo:	Gerar arquivo XML contendo dados dos artigos acadêmicos em um padrão solicitado.
    - Contexto:	N/A
    - Atores:	Desenvolvedores.
    - Recursos:	Arquivo XML modelo e arquivos JSON com dados do projeto.
    - Episódio: Gerar um arquivo XML nos padrões fornecidos pelo modelo, baseado nos dados contidos nos arquivos JSON.
    - Restrição: Não desobedecer ao padrão fornecido.
    - Exceção: Trancamento da disciplina, problemas na interpretação do trabalho, problemas de saúde com os desenvolvedores.

2) Especificação de Requisitos:

  - Requisitos Funcionais: 
    1.	Requisitos da versão existente são mantidos.

  - Requisitos Não Funcionais:
    1.	O sistema deve ser desenvolvido em Lua.
    2.	O sistema deve ler os dados de arquivos JSON.
    3.	Migrar o banco de dados para arquivos JSON.
    4.  Gerador XML deve ser criado.
    5.	Performance maior ou igual a anterior.

  - Requisitos Inversos:
    1.	O sistema não deve ter performance pior do que a versão existente.


3) Matriz de Rastreabilidade do Projeto (contendo apenas os módulos envolvidos nas modificações realizadas por nós):

![Matriz de Rastreabilidade dos Arquivos de Código-Fonte do Projeto WtranS](Documentos/matriz_rastreabilidade_codigo.JPG?raw=true "Title")


![Matriz de Rastreabilidade dos Arquivos Gerados do Projeto WtranS](Documentos/matriz_rastreabilidade_arquivos.JPG?raw=true "Title")


![Matriz de Rastreabilidade dos Requisitos do Projeto WtranS](Documentos/matriz_rastreabilidade_requisitos.JPG?raw=true "Title")


4) Arquitetura do Projeto (contendo apenas os módulos envolvidos nas modificações realizadas por nós):

 - Arquitetura Geral:
 
![Arquitetura Geral do Projeto WtranS](Documentos/Arquitetura/Arquitetura.jpg?raw=true "Title")

 - index.html:
 
![Arquitetura index.html do Projeto WtranS](Documentos/Arquitetura/index.html.jpg?raw=true "Title")

 - index.lp:
 
![Arquitetura index.lp do Projeto WtranS](Documentos/Arquitetura/index.lp.jpg?raw=true "Title")

 - papers_by_conference.lp:
 
![Arquitetura papers_by_conference.lp do Projeto WtranS](Documentos/Arquitetura/papers_by_conference.lp.jpg?raw=true "Title")

 - dao.lua:
 
![Arquitetura dao.lua do Projeto WtranS](Documentos/Arquitetura/dao.lua.jpg?raw=true "Title")

 - all_papers.lp:
 
![Arquitetura all_papers.lp do Projeto WtranS](Documentos/Arquitetura/all_papers.lp.jpg?raw=true "Title")

 - papers_cited.lp:
 
![Arquitetura papers_cited.lp do Projeto WtranS](Documentos/Arquitetura/papers_cited.lp.jpg?raw=true "Title")


5) Modelo ETVX (contendo apenas as informações envolvidas nas modificações realizadas por nós):

![Modelo ETVX do Projeto WtranS](Documentos/ETVX.JPG?raw=true "Title")

6) Cronograma do Projeto:

Veja aqui o [Cronograma](Documentos/cronograma.pdf?raw=true "Title") do projeto.

7) Evidências de Teste:

Segue abaixo uma comparação entre o projeto original e a versão por nós desenvolvida (DEV):

 - index.lp
 
    - Versão Original:
    
    ![Evidência de teste index.lp do Projeto Original WtranS](Documentos/teste/indexlp-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste index.lp do Projeto DEV WtranS](Documentos/teste/indexlp-dev.png?raw=true "Title")
    
 
 - all_papers.lp
 
    - Versão Original:
    
    ![Evidência de teste all_papers do Projeto Original WtranS](Documentos/teste/allpapers-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste all_papers do Projeto DEV WtranS](Documentos/teste/allpapers-dev.png?raw=true "Title")
    
    
 - papers_by_conference.lp - WTRANS13
 
    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS13 do Projeto Original WtranS](Documentos/teste/wtrans13-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS13 do Projeto DEV WtranS](Documentos/teste/wtrans13-dev.png?raw=true "Title")
    
  
  - papers_by_conference.lp - WTRANS14
  
    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS14 do Projeto Original WtranS](Documentos/teste/wtrans14-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS14 do Projeto DEV WtranS](Documentos/teste/wtrans14-dev.png?raw=true "Title")


- papers_by_conference.lp - WTRANS15

    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS15 do Projeto Original WtranS](Documentos/teste/wtrans15-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS15 do Projeto DEV WtranS](Documentos/teste/wtrans15-dev.png?raw=true "Title")
    

- papers_by_conference.lp - WTRANS16
 
    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS16 do Projeto Original WtranS](Documentos/teste/wtrans16-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS16 do Projeto DEV WtranS](Documentos/teste/wtrans16-dev.png?raw=true "Title")


- papers_by_conference.lp - WTRANS17
 
    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS17 do Projeto Original WtranS](Documentos/teste/wtrans17-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS17 do Projeto DEV WtranS](Documentos/teste/wtrans17-dev.png?raw=true "Title")
    

- papers_by_conference.lp - WTRANS18
 
    - Versão Original:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS18 do Projeto Original WtranS](Documentos/teste/wtrans18-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_by_conference.lp - WTRANS18 do Projeto DEV WtranS](Documentos/teste/wtrans18-dev.png?raw=true "Title")
    

- papers_cited.lp
 
    - Versão Original:
    
    ![Evidência de teste papers_cited.lp do Projeto Original WtranS](Documentos/teste/paperscited-original.png?raw=true "Title")
    
    - Versão DEV:
    
    ![Evidência de teste papers_cited.lp do Projeto DEV WtranS](Documentos/teste/paperscited-dev.png?raw=true "Title")
