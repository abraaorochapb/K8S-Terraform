Utilizaremos o Goldilocks para gerenciar o quanto de recurso iremos utilizar nas nossas aplicações, segue o guia:

Obs.: Necessário ter o Helm instalado

- Pegar os Values do Goldilocks no artifactHub, copiar para uma pasta desejada do seu server como um arquivo yaml
- Alterar para true nos values do VPA(Apenas o recommender) e do metrics-server (Caso não estejam instalados no Cluster)

adiciona o repo:                  
```helm repo add fairwinds-stable https://charts.fairwinds.com/stable```

no diretório que criou o arquivo yaml com os values:                    
```helm install goldilocks --namespace goldilocks -- create-namespace fairwinds.com/stable -f seu-arquivo.yaml```