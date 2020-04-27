# Instalação do Geru Widget

## Biblioteca javascript

A biblioteca javascript do Widget da Geru precisa ser incluída no corpo da página. O arquivo deve ser copiado para seu próprio site.

Exemplo de como a biblioteca deve ser carregada:

```html
<script src='/javascripts/geru-widget.js' type='text/javascript'></script>
```

## Elemento para montar o widget

O widget necessita de um elemento `container` na DOM no qual ele será inserido.

Sugerimos que seja um elemento HTML do tipo `<div>`, como no exemplo abaixo:

```html
<div id='widget-geru'></div>
```

## Função javascript

Para a montagem do widget, é necessário chamar a função javascript:

```javascript
geruWidget.configure
```

Abaixo os parâmetros que devem ser configurados:
* *container:* String, parâmetro obrigatório, ID na DOM do elemento no qual o iframe será inserido.
* *query:* String, parâmetro obrigatório, url fornecida pela Geru para uso do widget.
* *width:* Inteiro, Mínimo: 320 Padrão: 375, largura em pixels do iframe.
* *height:* Inteiro, Mínimo: 480 Padrão: 667, altura em pixels do iframe.

Exemplo de configuração para montar um widget dentro do elemento do DOM ID widget-geru  para a url `"https://tracking.stage-geru.com.br/api/v1/tracks?partner=geru-partner&redirect=https%3A%2F%2Fgeru.com.br%2Femprestimos%2Fparceiro%2Fwidget%2F%3Futm_medium%3Dmedium%26utm_content%3Dcontent%26utm_source%3Dsource"` com largura de `400` pixels e altura de `700` pixels.

```html
<script>
  let url = "https://tracking.stage-geru.com.br/api/v1/tracks?partner=geru-partner&redirect=https%3A%2F%2Fgeru.com.br%2Femprestimos%2Fparceiro%2Fwidget%2F%3Futm_medium%3Dmedium%26utm_content%3Dcontent%26utm_source%3Dsource";
  geruWidget.configure({
    container: 'geru-widget',
    query: url,
    width: 400,
    height: 700
  });
</script>
```


[Exemplo de aplicação do Widget em Blog](http://wwww.geru.com.br)

[Donwload da biblioteca Javascript](http://wwww.geru.com.br)
