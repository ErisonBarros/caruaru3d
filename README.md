
# MODELADOR GRÁFICO DO QGIS PARA ESTIMAR AS ALTURAS DAS EDIFICAÇÕES

  

O QGIS possui uma função chamada “modelador gráfico”, que permite automatizar rotinas de processamento através de uma interface prática de uso. Quando se trabalha com um SIG, a maioria das operações de análises não são isoladas, elas são parte de cadeias de operações que envolvem várias etapas. Usando um modelador gráfico, esses processos podem ser associados em um só sistema. O modelo é executado como um único algoritmo, poupando tempo, esforços e evitando possíveis erros no desenvolvimento de várias etapas separadas. O propósito do trabalho em questão é estimar as alturas das edificações para uma posterior modelagem 3d. As informações extraídas tem como base o MDE,

MDT e o arquivo vetorial dos limites das edificações. E o algoritmo utilizado é o seguinte:

  

> Primeiramente, utilizando a calculadora raster, a partir da subtração do MDE pelo MDT, é possível obter o “modelo de alturas” (MDA) da região.

Porém, com isso obtêm-se as alturas de toda extensão do raster, então é preciso direcionar esses dados para as edificações; • Gerar centroides dos polígonos através da ferramenta “centroies”, para garantir que o as alturas estejam referenciadas realmente dentro da edificação;

  

> Obter as alturas dos centroides em relação ao MDA, através da ferramenta “Amostrar os valores do raster”. Esta ferramenta cria uma coluna na tabela de atributos com os valores do raster referenciado;

  

> Unir as informações do arquivo de centroide (já com as devidas alturas), com o arquivo inicial dos polígonos de edificações através de um campo em comum de ligação.

  

Para automatizar esses processos no modulador, primeiramente é necessário a definição dos dados de entrada; neste caso são três arquivos: O arquivo vetorial de edificações, o raster de MDT e o raster de MDE. Depois é necessário definir o fluxo de trabalho. Usando os dados de entrada do modelo, o fluxo de trabalho é definido adicionando sequência das ferramentas mencionadas anteriormente e manipulando como os arquivos de entrada e os gerados vão se relacionar afim de obter o produto final. O modelo é salvo, e fica disponível na caixa de ferramentas de processamento do Qgis, ele executa todas etapas configuradas em um processo único.



Fonte:
https://docs.google.com/document/d/e/2PACX-1vTFrgf0weMJBYql2XkZzlGKWELsXjS2BnllWhIFKn_tabYeBA3i1CXOLUPzlwnBa7Iub06axMRVGZAo/pub


<img src="https://i.ibb.co/FgFJrBn/Capturar-1-JPG.jpg" alt="Capturar-1-JPG" border="0">

<img src="https://i.ibb.co/x3ZH4Cf/Capturar2.jpg" alt="Capturar2" border="0">


<img src="https://i.ibb.co/tsCsTC3/Capturar3.jpg" alt="Capturar3" border="0">


https://youtu.be/h54X-vxAe7A
![https://youtu.be/h54X-vxAe7A](https://youtu.be/h54X-vxAe7A)
