---
description: El término ISABOUT hace que las columnas coincidan con un grupo de uno o varios términos de búsqueda.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: ISABOUT Term
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5665e7bf62da4858cf2e7d68e65d0f42771903d55e3189db12f19cdd5414530d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969614"
---
# <a name="isabout-term"></a>ISABOUT Term

**Obsoleto**

Esta característica se ha quitado a Windows 8. Si escribe nuevas aplicaciones, evite usar esta característica en desuso. Si modifica las aplicaciones existentes, se recomienda encarecidamente quitar cualquier dependencia de esta característica.

El término ISABOUT hace que las columnas coincidan con un grupo de uno o varios términos de búsqueda. Tiene la sintaxis siguiente:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



El término OPCIONAL RANKMETHOD especifica el método de cálculo utilizado para clasificar los documentos que coinciden con uno o varios de los componentes. Si no se especifica RANKMETHOD, se usa el método de clasificación predeterminado del coeficiente de Figuracard.

El término ISABOUT puede tener uno o varios componentes. Las columnas especificadas en el [predicado CONTAINS](-search-sql-contains.md) se prueban en cada componente. El documento se incluye en los resultados si al menos uno de los componentes coincide. Las comas separan varios componentes.

La parte del componente tiene la sintaxis siguiente:


```
<match_term> [<weight_term>]
```



Puede usar el término PESO opcional para cambiar la importancia relativa de cada término dentro del término ISABOUT. Si no se aplica ningún término de peso, el peso predeterminado 1.0 está implícito.

En la tabla siguiente se describen los posibles tipos de términos de coincidencia.



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
<td>Una sola palabra sin espacios u otros signos de puntuación.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Wildcard (Carácter comodín)</td>
<td>Palabras o frases con el asterisco (*) agregado al final. Para obtener más información, <a href="-search-sql-wildcards.md">vea Using Wildcards in the CONTAINS Predicate</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>Ponderación de columnas ISABOUT

El término ISABOUT clasifica los documentos que coinciden en función de la coincidencia de cada documento con el conjunto de términos de coincidencia de la consulta. Puede usar la ponderación de columnas para dar más importancia a la coincidencia de algunos términos de coincidencia que otros. Cada término de coincidencia del término ISABOUT puede tener aplicado un valor de peso. El peso se aplica a un único término de coincidencia y se indica mediante la palabra clave "WEIGHT". El término WEIGHT tiene dos sintaxis alternativas:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



El valor de peso debe estar entre 0 y 1,0, sin más de tres posiciones decimales. Si se especifica un valor de peso fuera de este intervalo, se producirá un mensaje de error. El valor de clasificación sin ponderar de un término se multiplica por el valor de peso del término.

Si no se especifica ningún peso para un término de coincidencia, el valor predeterminado, 1.0, está implícito.

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se aplican pesos a los dos términos de coincidencia ISABOUT, usando la sintaxis larga y corta para los valores de peso.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



