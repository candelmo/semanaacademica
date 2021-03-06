Bibliometrix
================

## Bibliometrix

O pacote bibliometrix é uma “biblioteca” do R que fornece um conjunto de
ferramentas para pesquisa quantitativa em bibliometria e cienciometria.
A bibliometria é a aplicação de análises e estatísticas quantitativas a
publicações como artigos de periódicos e suas respectivas contagens de
citações.

# Instalação

Para instalação no console do R ou no R-Studio basta digitar o comando
`install.packages(bibliometrix)` e aguardar a instalação.

# Execução

Para a execução é necessário carregar o pacote e acionar sua execução

``` r
library(bibliometrix)
```

    ## To cite bibliometrix in publications, please use:
    ## 
    ## Aria, M. & Cuccurullo, C. (2017) bibliometrix: An R-tool for comprehensive science mapping analysis, Journal of Informetrics, 11(4), pp 959-975, Elsevier.
    ##                         
    ## 
    ## http:\\www.bibliometrix.org
    ## 
    ##                         
    ## To start with the shiny web-interface, please digit:
    ## biblioshiny()

``` r
biblioshiny()
```

    ## Loading required package: shiny

    ## 
    ## Listening on http://127.0.0.1:3489

O comando faz com que seja aberta uma janela do browser instalado no
computador e o aplicativo passe a ser executado no endereço `127.0.0.1`
(servidor local). Para a análise é necessário extrair dados de sua
pesquisa dos repositórios para carregar no Bibliometrix.

# Carga de dados

A carga de dados pode ser feita a partir de arquivos de consulta gerados
pelo Web of Science, Scopus, Dimensions, PubMed, Cochrane, nos formatos
Texto, EndNote ou Bibtex.

Poder ser carregados arquivos bibliometrix gerados em outras análises ou
ainda solicitar a conexão diretamente a fonte de informação DS
Dimensions ou da PubMed. Para isso é necessário ter uma conta em um
destes repositórios e informá-la junto com a senha como parâmetro de
conexão.

# Referências

DOMINGUES, Marco Antônio; BIANCHINI, Ilka Maria Escaliante; SANTOS, Luiz
Alberto Cardoso Dos; RUSSO, Suzana Leitão; LUCENA, Sadraque Eneas de
Figueiredo; SILVA, Daniel Pereira Da. Mapeamento da ciência com o pacote
R Bibliometrix: Uma aplicação no estudo de empreendedorismo acadêmico.
Anais do 9th ISTI - International Symposium on Technological Innovation,
\[S. l.\], v. Vol.9/n.1, p. 287–294, 2018. DOI:
10.7198/S2318-3403201800010033. Disponível em:
<http://www.api.org.br/conferences/index.php/ISTI2018/ISTI2018/paper/viewFile/612/291>.

MASSIMO, Aria; CUCCURULLO, Corrado. Package ‘bibliometrix’ version 3.0.3
Comprehensive Science Mapping Analysis. Disponível em:
<https://cran.r-project.org/web/packages/bibliometrix/bibliometrix.pdf>

PINTO, Darlene Pereira; HENCKLEIN, Gabriela Ribeiro; PAZIN, Drienne
Moreira; BORTOLOZZI, Mirian Batista de Oliveira; FEN, Amanda Trojan;
ERICH. Análise de decisão multicritério aplicado aos problemas do
contexto de saúde: uma contribuição bibliométrica. In: XXXIX ENCONTRO
NACIONAL DE ENGENHARIA DE PRODUÇÃO 2019, Santos - SP. Anais \[…\].
Santos - SP: ENEGEP, 2019. p. 1–17. Disponível em:
<http://www.abepro.org.br/biblioteca/TN_STP_292_1650_38058.pdf>.
