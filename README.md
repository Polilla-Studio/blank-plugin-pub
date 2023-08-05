Open links in a new tab using markdown
-

A common need when markdown is used is target the links to a new tab or window using **_blank attribute.** With this plugin you can use the filter ```| blank``` in twig and all the links detected in the text will have the _blank attribute. 

Use it after the ```| md``` filter


How to use it?
-


```  {{ sheet.description |md }} ```

```
<p>Este es un texto con un enlace: <a href="https://example.com">Enlace 1</a></p>
<p>Un enlace con segmento: <a href="https://example.com/pagina">Enlace 2</a></p>
<p>Un tercer enlace con parámetros: <a href="https://example.com/another-page?var=1&var=2">Enlace 3</a></p>
```

Just add ```|blank``` filter after the ```|md``` filter

```  {{ sheet.description |md |blank }} ```

This will attach the attribute **_blank** to all the links founded in the text

```
<p>Este es un texto con un enlace: <a href="https://example.com" target="_blank">Enlace 1</a></p>

<p>Un enlace con segmento: <a href="https://example.com/pagina" target="_blank">Enlace 2</a></p>

<p>Un tercer enlace con parámetros: <a href="https://example.com/another-page?var=1&var=2"  target="_blank">Enlace 3</a></p>
```
