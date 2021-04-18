---
description: El término próximo se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca de otro para que se reconozcan como coincidencia para el predicado CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: A corto plazo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360190"
---
# <a name="near-term"></a>A corto plazo

El término próximo se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca de otro para que se reconozcan como coincidencia para el predicado [Contains](-search-sql-contains.md) .

La sintaxis para el término próximo es:


```
<content_search_term> NEAR | ~ <content_search_term>
```



El término próximo se puede representar mediante la palabra clave "NEAR" o una tilde (~).

Cuando las palabras Unidas cerca de la consulta se encuentran en unas 50 palabras aproximadamente entre sí dentro de la columna en la que se busca, el término próximo devuelve una coincidencia. Cuanto más se acerquen las dos palabras, mayor será el rango calculado para el término próximo. Cuanto más lejos se encuentran las dos palabras, menor es el rango.

> [!Note]  
> El número de palabras entre los términos de búsqueda encontrados es aproximado y depende de la apariencia de las palabras irrelevantes, como "a" o "The", y cómo wordbreakers el texto de tokens. Puede ser inferior a 50.

 


En la tabla siguiente se describen los tipos de términos de búsqueda de contenido que se pueden usar con un término cercano en un predicado CONTAINS.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Una sola palabra sin espacios u otros signos de puntuación. No es necesario incluir comillas dobles.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
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
<td>Palabras o frases con el asterisco (*) agregados al final. Para obtener más información, vea <a href="-search-sql-wildcards.md">usar caracteres comodín en el predicado CONtains</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
> Si las palabras coincidentes especificadas con el término próximo se encuentran en la columna que se está buscando, pero se encuentran más allá de las 50 palabras, el resultado sigue siendo devuelto, pero tiene un [rango](-search-sql-understandingrelevancevalues.md) de 0.

 

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el encadenamiento de términos cercanos, usando las formas corto y largo del término:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Usar caracteres comodín en el predicado CONTAINS](-search-sql-wildcards.md)
</dt> </dl>

 

 



