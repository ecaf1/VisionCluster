# Vision Cluster

## Maximizando a Exatidão no Cuidado Ocular

### A cirurgia de catarata é um dos procedimentos oftalmológicos mais comuns e eficazes, realizada para restaurar a visão em pacientes que sofrem de catarata, uma condição onde a lente natural do olho torna-se opaca.

<img src="images/download.jpeg" width="600" style="margin-left: 200px;" />

### Apesar dos avanços tecnológicos e da eficácia comprovada da cirurgia, ainda existem desafios significativos na personalização do tratamento para alcançar os melhores resultados possíveis para cada paciente. Esses desafios incluem, mas não se limitam a:

-   ### Variação nas Medidas Oculares
-   ### Previsão de Necessidades de Lentes
-   ### Otimização dos Protocolos de Tratamento

### Riscos e complicações associados à cirurgia

-   ### Infecção ocular
-   ### Inflamação
-   ### Edema macular
-   ### Deslocamento do implante intraocular
-   ### Glaucoma
<img src="images/download (1).jpeg" width="600" style="margin-left: 200px;"/>

# Dados

### Neste projeto, utilizamos um conjunto de dados composto por medidas detalhadas dos olhos de pacientes submetidos à cirurgia de catarata.

-   ### AL = comprimento axial do olho
-   ### ACD = profundidade de câmara anterior
-   ### WTW = distância brando a branco
-   ### K1 = curvatura no meridiano menos curvo
-   ### K2 = curvatura no meridiano mais curvo

<img src="images/Screenshot from 2024-03-11 14-56-43.png" width="600" style="margin-left: 200px;"/>

## Redução de Dimensionalidade: PCA vs. t-SNE

### Para entender melhor a estrutura dos nossos dados e facilitar a visualização da dispersão dos grupos identificados pelos algoritmos de clustering, utilizamos duas técnicas poderosas de redução de dimensionalidade.

<img src="images/output.png" width="700" style="margin-left: 200px;"/>

## Técnica Utilizada: K-means

### Para segmentar os pacientes em grupos com características oculares similares, empregamos o algoritmo de clustering K-means. Este método é ideal para nosso propósito devido à sua simplicidade, eficiência e eficácia em agrupar dados com base em similaridades.

<img src="images/download.png" width="600" style="margin-left: 200px;"/>

## Determinação do Melhor Valor de K

### A escolha do número ótimo de clusters é crucial para a eficácia do K-means. Utilizamos o método do cotovelo, complementado pela análise de silhueta, para determinar o melhor valor de K. Ao plotar a soma das distâncias quadradas intra-cluster em função de diferentes valores de K, buscamos o ponto em que a curva começa a achatar, o "cotovelo".

<img src="images/Screenshot from 2024-03-10.png" width="600" style="margin-left: 200px;"/>


## Analise de resultado para K in [ 8, 9, 10 , 11]
### Utilizamos os algoritimos já comentados para redução da dimencionalidade.

<img src="images/k-8.png" width="600" style="margin-left: 200px;"/>
<img src="images/k-9.png" width="600" style="margin-left: 200px;"/>
<img src="images/k-10.png" width="600" style="margin-left: 200px;"/>
<img src="images/k-11.png" width="600" style="margin-left: 200px;"/>

## Ruido?
### Na projeção que utiliza o algoritimo PCA podemos notar alguns pontos distantes dos demais, será que podemos trata los como  "outliers"?
### Descrição dos dados:
<img src="images/describe.png" width="600" style="margin-left: 200px;"/>

## Segunda Técnica Utilizada: K-medoids
### Conhecido por sua robustez a outliers. Resultados para K in [8, 9 ,10, 11]
<img src="images/km-8.png" width="600" style="margin-left: 200px;"/>
<img src="images/km-9.png" width="600" style="margin-left: 200px;"/>
<img src="images/km-10.png" width="600" style="margin-left: 200px;"/>
<img src="images/km-11.png" width="600" style="margin-left: 200px;"/>



# Referências
- https://www.scikit-yb.org/en/latest/api/cluster/elbow.html
- 