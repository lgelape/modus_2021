# Exercício final

## Banco de dados

Vamos trabalhar com um banco de dados que traz informações de personagem da série "Star Wars". Ele vem originalmente no pacote `dplyr`, mas foi levemente modificado para essa atividade. A documentação deste banco de dados pode ser encontrada [neste link](https://dplyr.tidyverse.org/reference/starwars.html), em inglês.

```r
starwars <- read.csv2("https://raw.githubusercontent.com/lgelape/modus_2021/main/Bancos/starwars_trabalho.csv")
```
Use a função `head()` para dar uma olhada no conteúdo do banco.

```r
head(starwars)
```

## Estatísticas descritivas

**1. Faça tabelas de frequência absoluta e relativa da variáveis do mundo de origem (`homeworld`) desses personagens.**

**2. Agora, calcule as medidas de tendência central da variável altura (`height`). Como você descobriria esta medida no caso da variável espécie (`species`)?**

**3. Calcule um resumo das estatísticas descritivas da variável massa/peso (`mass`) (utilizando quaisquer das funções que aprendemos no Tutorial 2).**

**4. Faça um boxplot da variável massa/peso (`mass`) -- você deveria mexer em algum argumento para melhorar a visualização? Se sim, qual?**

## Estimação de parâmetros

Agora, vamos tirar uma amostra de 50 desses 87 personagens para estimar parâmetros de interesse.

```r
amostra_sw <- sample_n(starwars, size = 50)
```

**Estime a proporção de indivíduos do gênero feminino (`gender`) nesta amostra de personagens, calculando também o erro-padrão, margem de erro e intervalo de confiança (nível de confiança de 95% e 99%). Descreva os seus resultados.** 

**O que você pode falar sobre a influência do nível de confiança e do tamanho da amostra nessa estimativa?**

## Testes de hipótese

Agora, usaremos novas variáveis que criei para este banco: `humano`, que indica se o personagem é humano (`T`) ou não (`F`); e `motorista`, que indica se o personagem dirigiu alguma nave nos filmes da série.

**1. Assumindo que os pressupostos para a realização de um teste-t já foram atendidos, teste se a altura dos personagens humanas é diferente daquelas não-humanas, sob um nível de significância de 95%. Descreva seus resultados, apontando o valor da estatística teste, o p-valor e o significado do intervalo de confiança estimado pelo software.**

**2. Faça um teste qui-quadrado para analisar a associação entre as variáveis `humano` e `motorista`. Descreva os seus resultados, a partir de um nível de significância de 95%.**

**Em seguida, proceda ao mesmo teste para as variáveis gênero (`gender`) e `motorista`. Descreva seus resultados**
