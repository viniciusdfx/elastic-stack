## Contagem de Documentos

Eu odiava ver tutoriais que me ensinavam a baixar a aplicação para logo em seguida fazer a subida e executar alguma outra coisa. Chegou a hora de dar o troco ! Vamos subir novamente a nossa instância de Elasticsearch para realizar a contagem de documentos existentes em nossos índices:

```
nohup ./elasticsearch &
```

Vamos utilizar a API **_count** para contar quantos documentos existem no index "mycompany":

```
curl -XGET http://localhost:9200/mycompany/_count?pretty
```

Caso você queira contar a quantidade de documentos totais em seu Elasticsearch, é só retirar o index mycompany da pesquisa:

```
curl -XGET http://localhost:9200/_count?pretty
```

Próximo: [Entendendo melhor os contextos](/pages/contexts.md)
