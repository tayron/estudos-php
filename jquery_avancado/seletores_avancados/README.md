# Seletores Avançados com Jquery

A biblioteca Jquery disponibiliza uma sentença para selecionar elementos no DOM da página. 
O seletor acessa os elementos cujo valor do atributo 
id for especificado no parâmetro. A sintaxe deste atributo segue a mesma 
regra do CSS, onde o id do elemento é precedido por '#', nome de um class é precedido
de '.', etc..

<br />

**Exemplo**
```php
$('#email').val()
```

<br />

O exemplo acima recupera o valor de um elemento HTML que possua o ID "email". 
**Observação:** Em um documento DOM não se deve ter um ID para mais de um elemento.

<br />

Seguindo as mesmas regras do CSS também é possível selecionar elementos através de sua class.

<br />

**Exemplo**
```php
$('.campos').val()
```

<br />

Seguindo os mesmos conceitos do CSS é possível fazer seleção avançadas, utilizando 
condicionais.

<br />

**Exemplo:** Vamos selecionar todos os links que apontem para a url site.com.br
```php
$("a[href='site.com']")

```

<br />
Um outro exemplo seria buscar todos os campos input de um formulário para aplicar 
um determinado estilo css.
```php
$("input[type='text']").css('color', '#F00');

```

<br />

Referências: 

* https://pt.wikipedia.org/wiki/JQuery
* http://www.devmedia.com.br/introducao-aos-seletores-da-jquery/27362