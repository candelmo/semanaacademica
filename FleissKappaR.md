Fleiss Kappa no R
================

## O teste

O teste de concordância Kappa (K), ou **coeficiente de Kappa**, foi
proposto por Jacob Cohen em 1960, com a finalidade de medir o grau de
concordância entre proporções derivadas de amostras dependentes. Ele
também é utilizado para determinar concordância entre avaliadores de uma
revisão sistemática.

## O código

Carregando o pacote, se for a primeira vez que roda o pacote será
necessário instalá-lo também.

``` r
library(irr)
```

    ## Loading required package: lpSolve

## Determinando os valores de avaliação

Incluindo os valores no dataset

``` r
avaliador1<-c(1,3,3,2,1,5,1,2,2,3,3,2)
avaliador2<-c(1,3,3,2,4,5,1,2,2,3,3,2)
avaliador3<-c(1,3,3,2,4,5,1,2,2,3,3,2)
avaliador4<-c(1,3,3,2,4,5,1,4,2,5,3,2)
avaliador5<-c(2,3,3,2,4,5,1,4,2,5,3,2)
avaliador6<-c(2,3,3,2,4,5,1,4,2,5,3,2)
data<-data.frame(avaliador1, avaliador2, avaliador3, avaliador4, avaliador5, avaliador6)
```

## Visão das avaliações carregadas

No exemplo foram 12 avaliações realizadas por 6 avaliadores. As
avaliações podem ser avaliações de pacientes em estágios diferentes de
doença (1-São até 5-Estágio Terminal) ou qualidade de um determinado
artigo para uma revisão sistemática (1-Baixo até 5-Alta) ou mesmo outro
critério que se queira definir. A escala também pode ser reduzida
(0-Reprovado, 1-Aprovado).

| avaliador1 | avaliador2 | avaliador3 | avaliador4 | avaliador5 | avaliador6 |
| ---------: | ---------: | ---------: | ---------: | ---------: | ---------: |
|          1 |          1 |          1 |          1 |          2 |          2 |
|          3 |          3 |          3 |          3 |          3 |          3 |
|          3 |          3 |          3 |          3 |          3 |          3 |
|          2 |          2 |          2 |          2 |          2 |          2 |
|          1 |          4 |          4 |          4 |          4 |          4 |
|          5 |          5 |          5 |          5 |          5 |          5 |
|          1 |          1 |          1 |          1 |          1 |          1 |
|          2 |          2 |          2 |          4 |          4 |          4 |
|          2 |          2 |          2 |          2 |          2 |          2 |
|          3 |          3 |          3 |          5 |          5 |          5 |
|          3 |          3 |          3 |          3 |          3 |          3 |
|          2 |          2 |          2 |          2 |          2 |          2 |

## Calculando o índice Kappa Fleiss

``` r
kappam.fleiss(data, detail=TRUE)
```

    ##  Fleiss' Kappa for m Raters
    ## 
    ##  Subjects = 12 
    ##    Raters = 6 
    ##     Kappa = 0.774 
    ## 
    ##         z = 19.4 
    ##   p-value = 0 
    ## 
    ##    Kappa      z p.value
    ## 1  0.721  9.673   0.000
    ## 2  0.783 10.502   0.000
    ## 3  0.879 11.793   0.000
    ## 4  0.606  8.134   0.000
    ## 5  0.771 10.350   0.000

Em 1973 Fleiss e Kappa determinaram valores de interpretação possíveis
em função dos resultados, nesta função observe o valor de `Kappa` a ser
interpretado conforme os valores abaixo:

| faixas    | interpretacao               |
| :-------- | :-------------------------- |
| \<0       | Ausência de concordância    |
| 0-0,19    | Concordância Pobre          |
| 0,20-0,39 | Concordância Leve           |
| 0,40-0,59 | Concordância Moderada       |
| 0,60-0,79 | Concordância Substantiva    |
| 0,80-1,00 | Concordância Quase perfeita |

O índice permite observar o nível de concordância geral e o individual
de cada categoria de análise, no nosso caso usamos uma escala de 5
categorias, o `p-valor` em qualquer caso precisa ser 0.

## Referências

GAMER, Matthias et all. Package ‘irr’ - Various Coefficients of
Interrater Reliability and Agreement. Disponível em:
<https://cran.r-project.org/web/packages/irr/irr.pdf>

SILVA, Rebeca de Souza e; PAES, Ângela Tavares. ￼Por Dentro da
Estatística: teste de concordância de Kappa. Educ. Contin. Saúde
einstein, \[S. l.\], v. 10, n. 4, p. 165–166, 2012. Disponível em:
<http://apps.einstein.br/revista/arquivos/PDF/2715-165-166.pdf>.
