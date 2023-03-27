## Resilia: Projeto M4 - Visualizando a situação

CONTEXTO: Temos um problema e precisaremos da sua ajuda para resolver! Acumulamos alguns conjuntos de dados e não conseguimos ter uma visão padronizada desses dados. O conjunto de dados disponíveis podem ser encontrados aqui:https://drive.google.com/drive/folders/1F9Rwbzzz4LJCxZU-mTR4JqDT_2vJ7-sC?usp=sharing.

## 🧭 OBJETIVO

Nesse projeto você e sua squad deverão montar um dashboard com base no conjunto de dados escolhidos por vocês, a fim de realizar uma apresentação com a exploração dos dados. Escolhemos pela análise de dados relacionado ao software de gestão de direitos digitais Steam. Por essa plataforma, que é a mais popular dessa categoria, é possível comprar, armazenar e executar jogos para computador.
Dessa forma, com base no banco de dados fornecido previamente, executamos o software MySQL Workbench e Power BI.

# 🔧 Tecnologias usadas:

    Power BI
    Workbench

## 📝 Etapas

    Busca dos dados;
    Criação de perguntas;
    Tratamento dos dados;
    Criação de gráficos;
    Criação do diagrama de entidade e relacionamento;
    Criação da Apresentação.

## 📋 Perguntas

 Durante o Brainstorm sobre perguntas que podem ser respondidas pelos dados selecionamos as seguintes perguntas:

    •	Quais os 5 jogos mais jogados?
    •	Quais os 5 jogos mais caros?
    •	Quais os 5 jogos mais mal avaliados?
    •	Qual desenvolvedora tem mais jogos na steam? (5 maiores)
    •	Qual a quantidade de jogos em cada gênero? (10 maiores)

## 🔖 RESULTADOS

Obtivemos o seguinte Dashboard 

![DASHBOARD](https://github.com/raycadilhe/squad-modulo4-resilia/blob/main/dashboard.JPG?raw=true)


EXECUTAMOS OS SEGUINTES FILTROS 

    •	Quais os 5 jogos mais jogados?
            SELECT name AS 'Titulo do Jogo', average_playtime AS 'Media de tempo jogado' FROM steam
            ORDER BY average_playtime DESC
            LIMIT 5
            
![PERGUNTA1](https://user-images.githubusercontent.com/115670321/228081553-ee2dc6e3-c92d-46be-87d8-ef4703f56426.png)


    •	Quais os 5 jogos mais caros?
            SELECT name AS 'Titulo do jogo', price AS 'Preco' FROM steam
            ORDER BY price DESC
            LIMIT 5
            
![PERGUNTA2](https://user-images.githubusercontent.com/115670321/228081456-81d3d792-3d1c-42b9-ae96-1c6d43345a40.png)


    •	Quais os 5 jogos mais mal avaliados?
            SELECT name AS 'Titulo do Jogo', negative_ratings AS 'Avaliacoes negativas' FROM steam
            ORDER BY negative_ratings DESC
            LIMIT 5
            
![PERGUNTA3](https://user-images.githubusercontent.com/115670321/228081422-e79713c9-1fa6-4f98-a361-b4010364c01d.png)


    •	Qual desenvolvedora tem mais jogos na steam? (5 maiores)
            SELECT developer AS 'Desenvolvedora', COUNT(name) AS Quantidade_jogos FROM steam
            GROUP BY developer
            ORDER BY Quantidade_jogos DESC
            LIMIT 5
            
![PERGUNTA4](https://user-images.githubusercontent.com/115670321/228081170-2151de09-c1f1-41d4-98f9-63667505df4e.png)


    
    •	Qual a quantidade de jogos em cada gênero? (10 maiores)
            SELECT genres AS Genero, COUNT(genres) AS Quantidade_jogos FROM steam
            GROUP BY Genero
            ORDER BY Quantidade_jogos DESC
            LIMIT 10
            
![PERGUNTA5](https://user-images.githubusercontent.com/115670321/228081094-9aefd323-dd77-4e30-9ad0-add6e5b9bdba.png)



## 🤝 DESENVOLVEDORES

    Beatriz Melo:  Desenvolvimento de perguntas e códigos 
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&%22width=%2260&link=https:https://www.linkedin.com/in/lucascanella-dados/)](https://br.linkedin.com/in/beatrizmelop/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white%22width=%2260)](https://github.com/SuzBarbosa)
    
    Carol Bentes: Desenvolvimento de perguntas e criação da apresentação.
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https:https://www.linkedin.com/in/lucascanella-dados/)](https://www.linkedin.com/in/caroline-bentes-89ba28160/)
         
    
    Martha Lucena: Desenvolvimento de perguntas e criação da apresentação. 
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https:https://www.linkedin.com/in/lucascanella-dados/)](https://br.linkedin.com/in/martha-lucena-%F0%9F%8F%B3%EF%B8%8F%E2%80%8D%F0%9F%8C%88-54866195?trk=public_profile_browsemap)
    
    Rayssa Cadilhe: Desenvolvimento de perguntas, códigos no MySQL e diagrama de entidade e relacionamento.
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https:https://www.linkedin.com/in/lucascanella-dados/)](https://www.linkedin.com/in/rayssacadilhe/)
    
    Suzana Barbosa: Desenvolvimento de perguntas e criação do README
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https:https://www.linkedin.com/in/lucascanella-dados/)](https://www.linkedin.com/in/suzanacobarbosa)
   

