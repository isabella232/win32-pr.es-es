---
description: El término NEAR se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca unos de otros para que se reconozcan como coincidencias para el predicado CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: NEAR Term
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c43d6e3554722ebeb65d2789d07adb521177a986
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631823"
---
# <a name="near-term"></a>NEAR Term

El término NEAR se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca unos de otros para que se reconozcan como coincidencias para el [predicado CONTAINS.](-search-sql-contains.md)

La sintaxis del término NEAR es:


```
<content_search_term> NEAR | ~ <content_search_term>
```



El término NEAR se puede representar mediante la palabra clave "NEAR" o mediante una tilde (~).

Cuando las palabras unidas por NEAR en la consulta se encuentran dentro de aproximadamente 50 palabras entre sí dentro de la columna en la que se está buscando, el término NEAR devuelve una coincidencia. Cuanto más cerca estén las dos palabras, mayor será el rango calculado para el término NEAR. Cuanto más lejos estén las dos palabras, menor es la clasificación.

> [!Note]  
> El número de palabras entre los términos de búsqueda encontrados es aproximado y depende de la apariencia de las palabras ruidosas, como "a" o "the", y de la forma en que los buscadores de palabras tokenizan texto. Puede ser menor que 50.

 


En la tabla siguiente se describen los tipos de términos de búsqueda de contenido que se pueden usar con un término NEAR en un predicado CONTAINS.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descripción</th>
<th>Ejemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Una sola palabra sin espacios u otros signos de puntuación. No son necesarias comillas dobles.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Frase</td>
<td>Varias palabras o espacios incluidos.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Wildcard (Carácter comodín)</td>
<td>Palabras o frases con el asterisco (*) agregado al final. Para obtener más información, <a href="-search-sql-wildcards.md">vea Usar caracteres comodín en el predicado CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Si las palabras de coincidencia especificadas con el término NEAR se encuentran en la columna en la que se busca, pero están más lejos que 50 palabras, el resultado se devuelve, pero tiene un rango de 0. [](-search-sql-understandingrelevancevalues.md)

 

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el encadenamiento de términos NEAR, usando las formas cortas y largas del término:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Usar caracteres comodín en el predicado CONTAINS](-search-sql-wildcards.md)
</dt> </dl>

 

 



