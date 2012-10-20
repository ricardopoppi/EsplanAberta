# EsplanABERTA

EsplanABERTA é um projeto que envolve a visualização dos datasets abertos pelo Governo Federal num mapa da Esplanada dos Ministérios, em Brasília. Só aparecerão no mapa datasets divulgados nos formatos xml, csv, zip+csv e json.  
Consiste em um script que faz a leitura das APIs de catálogos de dados que estejam indexando datasets do governo federal (como dados.gov.br) e uma interface que apresenta um mapa em svg da Esplanada com ícones referentes aos datasets.  
A idéia é mostrar quais minstérios tem dados abertos e que tipo de dados abertos estão referenciados.

Inicialmente, o script de leitura das APIs poderá trabalhar com o portal de dados abertos do governo federal - dados.gov.br - baseado em CKAN \o/ e com a API disponível. Funções do script:

- Leitura do conjunto de datasets que coincidem com os formatos abertos pré definidos (xml, csv, zip+csv e json) 
> exemplo: http://dados.gov.br/api/search/dataset?q=res_format:"csv"

- Leitura, por dataset identificado, do conjunto de tags e grupos associados a ele 
> exemplo: CGU, Trabalho

- Associar cada tag ou grupo obtido com um conjunto de palavras pré-definido e associado aos prédios na Esplanada 
> exemplo: Ministério do Trabalho associado a "trabalho", "emprego", ... / Ministério da Saúde associado a "saúde", "sus", "datasus", ...

- Quando houver "match" entre as Tags e Groups obtidos no portal de dados abertos o dataset é visualizado próximo ao prédio, já com o link para o recurso (dataset)

Futuramente, o projeto poderá ler datasets presentes em sites de ministérios ou orgãos que não estejam cadastrados em catálogos de dados abertos com API. Para isso poderá ser construido um script "meio" que faça screen scraping de bases de dados presentes nesses sites, guarde essa informação em bases locais e disponibilize por API para o script do EsplanABERTA. Com isso o EsplanABERTA permitirá visualização e links para recursos de dados abertos que não estejam cadastrados em catálogos.


Obs.: saiba mais sobre o formato SVG --> link para o working group de SVG do W3C http://www.w3.org/Graphics/SVG/ 
Referências: http://5stardata.info/