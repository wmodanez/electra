# electra

## Geração do dataset da Wikipedia:

1. Fazer o download da versão mais atual do dump da [wikipedia](https://dumps.wikimedia.org/ptwiki/latest/ptwiki-latest-pages-articles.xml.bz2);
2. Utilizar a versão modificada do script WikiExtractor para transformar o xml em um documento json;
3. Ler o arquivo json com o comando abaixo ao invés de usar o pandas devido ao tamanho do arquivo:

```python
with open('text/wiki.txt') as json_file:      
    data = json_file.readlines()
    data = list(map(json.loads, data))
```

4. Inserir o list gerado em um dataframe;
5. Salvar o dataframe em formato csv.
