# Resilia [Data Analytics]: Projeto M4 - Visualizando a situação

CONTEXTO: Temos um problema e precisaremos da sua ajuda para resolver! Acumulamos alguns conjuntos de dados e não conseguimos ter uma visão padronizada desses dados. O conjunto de dados disponíveis podem ser encontrados aqui:https://drive.google.com/drive/folders/1F9Rwbzzz4LJCxZU-mTR4JqDT_2vJ7-sC?usp=sharing.

# 🧭 OBJETIVO

⇨ Nesse projeto você e sua squad deverão montar um dashboard com base no conjunto de dados escolhidos por vocês, a fim de realizar uma apresentação com a exploração dos dados. 

Nosso projeto tem como objetivo a realização de uma análise de dados relacionado ao software de gestão de direitos digitais Steam. Por essa plataforma, que é a mais popular dessa categoria, é possível comprar, armazenar e executar jogos para computador.
Dessa forma, com base no banco de dados fornecido previamente, executamos o software MySQL filtragem de dados. 

# 🔧 Tecnologias usadas:

    Power BI
    Workbench

# 📝 Etapas

    Busca dos dados;
    Criação de perguntas;
    Tratamento dos dados;
    Criação de gráficos;
    Criação do diagrama de entidade e relacionamento;
    Criação da Apresentação.

# 📋 Perguntas

 Durante o Brainstorm sobre perguntas que podem ser respondidas pelos dados selecionamos as seguintes perguntas:

    •	Quais os 5 jogos mais jogados?
    •	Quais os 5 jogos mais caros?
    •	Quais os 5 jogos mais mal avaliados?
    •	Qual desenvolvedora tem mais jogos na steam? (5 maiores)
    •	Qual a quantidade de jogos em cada gênero? (10 maiores)

# 🔖 RESULTADOS

Obtivemos o seguinte Dashboard 

<img src="(https://github.com/raycadilhe/squad-modulo4-resilia/blob/main/dashboard.JPG?raw=true)" width="90" height="50" />


EXECUTAMOS OS SEGUINTES FILTROS 

    •	Quais os 5 jogos mais jogados?
            SELECT name AS 'Titulo do Jogo', average_playtime AS 'Media de tempo jogado' FROM steam
            ORDER BY average_playtime DESC
            LIMIT 5

    •	Quais os 5 jogos mais caros?
            SELECT name AS 'Titulo do jogo', price AS 'Preco' FROM steam
            ORDER BY price DESC
            LIMIT 5

    •	Quais os 5 jogos mais mal avaliados?
            SELECT name AS 'Titulo do Jogo', negative_ratings AS 'Avaliacoes negativas' FROM steam
            ORDER BY negative_ratings DESC
            LIMIT 5

    •	Qual desenvolvedora tem mais jogos na steam? (5 maiores)
            SELECT developer AS 'Desenvolvedora', COUNT(name) AS Quantidade_jogos FROM steam
            GROUP BY developer
            ORDER BY Quantidade_jogos DESC
            LIMIT 5

    
    •	Qual a quantidade de jogos em cada gênero? (10 maiores)
            SELECT genres AS Genero, COUNT(genres) AS Quantidade_jogos FROM steam
            GROUP BY Genero
            ORDER BY Quantidade_jogos DESC
            LIMIT 10


# NOSSA EQUIPE

    Beatriz Melo:  Desenvolvimento de perguntas, códigos e criação do README.
    
    Carol Bentes: Desenvolvimento de perguntas e criação da apresentação.
    
    Martha Lucena: Desenvolvimento de perguntas e criação da apresentação. 
    
    Rayssa Cadilhe: Desenvolvimento de perguntas, códigos no MySQL e diagrama de entidade e relacionamento.
    
    Suzana Barbosa: Desenvolvimento de perguntas e criação do dashboard.
   

