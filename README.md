# Desafio Imersão IA Alura + Google

Esse notebook irá buscar pelo user (variável `letterboxd_username`) no site letterboxd e com base nos seus reviews irá gerar 5 recomendações de filmes no idioma definido (variável `language`).

Letterboxd scraper baseado nesse [artigo](https://medium.com/@alf.19x/letterboxd-friends-ranker-simple-movie-recommendation-system-80a38dcfb0da).

Desafios encontrados:
- O modelo recomendava filmes listados na amostra de reviews, corrigido incluindo uma restrição explicita no prompt para não incluir filmes já avaliados.
- O modelo recomendava filmes baseados em filmes mal avaliados, corrigido ensinando ao modelo o que é uma nota baixa e o que é uma nota alta, também foi adicioando um limite mínimo de nota que ele deva usar na recomendação.
- Usuários com muitos reviews poderiam usar muitos tokens, mitigado usando uma amostra aleatória de 15 tokens (configurável pela variável `sample_size`)
