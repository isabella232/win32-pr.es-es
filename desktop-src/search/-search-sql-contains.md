---
description: El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907743"
---
# <a name="contains-predicate"></a>Predicado CONTAINS

El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto. El predicado CONTAINS tiene características para buscar palabras coincidentes, buscar coincidencias de formas con inflexión de palabras, buscar mediante caracteres comodín y realizar búsquedas con proximidad. También puede aplicar pesos en un predicado CONTAINS para establecer la importancia de las columnas en las que se encuentra el término de búsqueda. El predicado CONTAINS es más adecuado para las coincidencias exactas, al contrario que el predicado [FREETEXT](-search-sql-freetext.md) , que es más adecuado para buscar documentos que contengan combinaciones de las palabras de búsqueda distribuidas en toda la columna. Las búsquedas no distinguen entre mayúsculas y minúsculas.

A continuación se muestra la sintaxis básica del predicado CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

La \_ referencia de columna fulltext es opcional. Con él, puede limitar la búsqueda a una sola columna o a un grupo de columnas en el que se prueba el predicado CONTAINS. Cuando la columna fulltext se especifica como "ALL" o " \* ", se busca en todas las propiedades de texto indizadas. Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos. El nombre de la columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado, y debe separarlo de la condición mediante una coma. Si no se especifica ninguna columna de texto completo, se usa la columna System. Search. Contents, que es el cuerpo del documento.

La parte LCID del predicado especifica la configuración regional de la búsqueda. Esto indica al motor de búsqueda que utilice el separador de palabras y las formas con inflexión adecuadas para la consulta de búsqueda. Para especificar la configuración regional, proporcione el identificador de código de idioma (LCID) estándar de Windows. Por ejemplo, 1033 es el LCID para Estados Unidos-English. Coloque el LCID como el último elemento dentro de los paréntesis de la cláusula Contains. Para obtener información importante acerca de la búsqueda y los lenguajes, consulte [uso de búsquedas localizadas](-search-sql-usinglocsearches.md).

> [!NOTE]  
> La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.

La parte de la condición Contains \_ debe ir entre comillas simples para palabras individuales o comillas dobles para frases, y consta de uno o varios términos de búsqueda de contenido que se combinan mediante los operadores lógicos **and** u **or**. Puede usar el operador unario opcional **no** después de un operador **and** para negar el valor lógico de un término de búsqueda de contenido.

> [!NOTE]  
> El operador **Not** solo puede aparecer después **de y**. No se puede usar el operador **Not** si solo hay una condición de coincidencia o después del operador **or** .

Puede usar paréntesis para agrupar y anidar términos de búsqueda de contenido. En la tabla siguiente se describe el orden de prioridad de los operadores lógicos.

| Orden (precedencia) | Operador lógico |
|--------------------|------------------|
| Primero (más alto)    | **NOT**          |
| Segundo             | **AND**          |
| Tercer (el más bajo)     | **OR**           |

Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado. Por ejemplo, (A **y** B) **y** (C **y** d) se pueden calcular (B **y** C) **y** (A **y** D) sin ningún cambio en el resultado lógico.

En la tabla siguiente se describen los tipos de términos de búsqueda de contenido.

<!-- markdownlint-disable MD033 -->
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
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Columna de texto completo</td>
<td>Nombre de la columna de propiedad con la que se va a hacer coincidir la consulta restante.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Palabras, frases y cadenas comodín combinadas mediante los operadores booleanos <strong>and</strong>, <strong>or</strong>o <strong>Not</strong>. Incluya los términos booleanos entre comillas dobles.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Near</td>
<td>Palabras, frases o caracteres comodín separados por la función NEAR. Para obtener más información, vea <a href="-search-sql-near.md">Near term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Coincide con una palabra y con las versiones con inflexión de esa palabra. Para obtener más información, vea el <a href="-search-sql-formsof.md">término FORMSOF</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Combina los resultados de búsqueda de coincidencias en varios términos de palabras, frases o caracteres comodín. Opcionalmente, se puede ponderar cada término de búsqueda. Opcionalmente, puede especificar el método de cálculo de clasificación, que combina los pesos y el número de elementos que coinciden con el documento. Para obtener más información, consulte <a href="-search-sql-isabout.md">isabout term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Esta sección contiene los siguientes temas:

- [Usar caracteres comodín en el predicado CONTAINS](-search-sql-wildcards.md)
- [Términos de FORMs](-search-sql-formsof.md)
- [Término ISABOUT](-search-sql-isabout.md)
- [A corto plazo](-search-sql-near.md)

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[Cláusula WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Conceptual

[Predicados de texto completo](-search-sql-fulltextpredicates.md)

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
