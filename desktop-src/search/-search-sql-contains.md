---
description: El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2885187d0dd25f38e6bbf40b3259164f0aa91e05
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625291"
---
# <a name="contains-predicate"></a>Predicado CONTAINS

El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto. El predicado CONTAINS tiene características para buscar coincidencias de palabras, buscar coincidencias con formas de palabras inflectionales, buscar con caracteres comodín y buscar mediante proximidad. También puede aplicar ponderaciones en un predicado CONTAINS para establecer la importancia de las columnas donde se encuentra el término de búsqueda. El predicado CONTAINS es más adecuado para coincidencias exactas, a diferencia del predicado [FREETEXT,](-search-sql-freetext.md) que es más adecuado para buscar documentos que contengan combinaciones de las palabras de búsqueda repartidas por la columna. Las búsquedas no distinguen entre mayúsculas y minúsculas.

A continuación se muestra la sintaxis básica del predicado CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

La referencia de columna \_ de texto completo es opcional. Con él, puede limitar la búsqueda a una sola columna o a un grupo de columnas en el que se prueba el predicado CONTAINS. Cuando la columna fulltext se especifica como "ALL" o " ", se buscan todas las \* propiedades de texto indizado. Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos. El nombre de columna puede ser un identificador normal o [delimitado,](-search-sql-identifiers.md)y debe separarlo de la condición mediante una coma. Si no se especifica ninguna columna de texto completo, se usa la columna System.Search.Contents, que es el cuerpo del documento.

La parte LCID del predicado especifica la configuración regional de búsqueda. Esto indica al motor de búsqueda que use el separador de palabras adecuado y los formularios inflectionales para la consulta de búsqueda. Para especificar la configuración regional, proporcione el Windows de código de idioma estándar (LCID). Por ejemplo, 1033 es el LCID para Estados Unidos inglés. Coloque el LCID como el último elemento entre paréntesis de la cláusula CONTAINS. Para obtener información importante sobre la búsqueda y los idiomas, vea [Usar búsquedas localizadas.](-search-sql-usinglocsearches.md)

> [!NOTE]  
> La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.

La parte de condición contains debe incluirse entre comillas simples para palabras simples o comillas dobles para frases, y consta de uno o varios términos de búsqueda de contenido que se combinan mediante los operadores \_ lógicos **AND** o **OR**. Puede usar el operador unario **opcional NOT** después de un operador **AND** para negar el valor lógico de un término de búsqueda de contenido.

> [!NOTE]  
> El **operador NOT** solo puede producirse después de **AND.** No puede usar el **operador NOT** si solo hay una condición de coincidencia o después del **operador OR.**

Puede usar paréntesis para agrupar y anidar términos de búsqueda de contenido. En la tabla siguiente se describe el orden de prioridad de los operadores lógicos.

| Order (precedencia) | Operador lógico |
|--------------------|------------------|
| First (más alto)    | **NOT**          |
| Segundo             | **AND**          |
| Tercera (más baja)     | **OR**           |

Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado. Por ejemplo, (A **AND** B) **AND** (C **AND** D) se puede calcular (B **AND** C) **AND** (A **AND** D) sin ningún cambio en el resultado lógico.

En la tabla siguiente se describen los tipos de términos de búsqueda de contenido.

<!-- markdownlint-disable MD033 -->
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
<col  />
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
<td>Palabras o frases con el asterisco (*) agregado al final. Para obtener más información, <a href="-search-sql-wildcards.md">vea Usar caracteres comodín en el predicado CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Nombre de columna de propiedad con el que se va a coincidir con la consulta restante.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Palabras, frases y cadenas de caracteres comodín combinadas mediante los operadores <strong>booleanos AND</strong>, <strong>OR</strong>o <strong>NOT</strong>. Incluya los términos booleanos entre comillas dobles.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Palabras, frases o caracteres comodín separados por la función NEAR. Para obtener más información, vea <a href="-search-sql-near.md">NEAR Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Coincide con una palabra y las versiones desinflectionales de esa palabra. Para obtener más información, vea <a href="-search-sql-formsof.md">TÉRMINO FORMSOF</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Combina los resultados correspondientes en varios términos de búsqueda de palabras, frases o caracteres comodín. Opcionalmente, cada término de búsqueda se puede ponderar. Opcionalmente, puede especificar el método de cálculo de rango, que combina las ponderaciones y el número de elementos con los que coincide el documento. Para obtener más información, vea <a href="-search-sql-isabout.md">Isabout Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
- [Término FORMSOF](-search-sql-formsof.md)
- [Término de ISABOUT](-search-sql-isabout.md)
- [NEAR Term](-search-sql-near.md)

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[Cláusula WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Conceptual

[Predicados de texto completo](-search-sql-fulltextpredicates.md)

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
