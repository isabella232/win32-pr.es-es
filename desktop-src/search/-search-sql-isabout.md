---
description: El término ISABOUT coincide con las columnas de un grupo de uno o más términos de búsqueda.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Término ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808936"
---
# <a name="isabout-term"></a>Término ISABOUT

**En desuso**

Esta característica se ha quitado de Windows 8. Si escribe nuevas aplicaciones, evite usar esta característica en desuso. Si modifica las aplicaciones existentes, le recomendamos encarecidamente que quite todas las dependencias de esta característica.

El término ISABOUT coincide con las columnas de un grupo de uno o más términos de búsqueda. Tiene la siguiente sintaxis:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



El término RANKMETHOD opcional especifica el método de cálculo que se usa para clasificar los documentos que coinciden con uno o varios de los componentes. Si no se especifica RANKMETHOD, se usa el método predeterminado de clasificación de coeficientes de Jaccard.

El término ISABOUT puede tener uno o más componentes. Las columnas especificadas en el predicado [Contains](-search-sql-contains.md) se prueban en cada componente. El documento se incluye en los resultados si al menos uno de los componentes coincide con. Las comas separan varios componentes.

La parte del componente tiene la siguiente sintaxis:


```
<match_term> [<weight_term>]
```



Puede usar el término de PONDERAción opcional para cambiar la importancia relativa de cada término dentro del término ISABOUT. Si no se aplica ningún término de peso, se implica el peso predeterminado 1,0.

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



 

## <a name="isabout-column-weighting"></a>Ponderación de columnas de ISABOUT

El término ISABOUT clasifica los documentos coincidentes en función del grado de coincidencia de cada documento con el conjunto de términos coincidentes de la consulta. Puede usar la ponderación de columnas para hacer más importante la coincidencia de algunos términos de coincidencia que otros. Cada término coincidente en el término ISABOUT puede tener un valor de peso aplicado. El peso se aplica a un único término de coincidencia y se indica mediante la palabra clave "WEIGHT". El término de PONDERAción tiene dos sintaxis alternativas:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



El valor de peso debe estar entre 0 y 1,0, sin más de tres posiciones decimales. Si se especifica un valor de peso fuera de este intervalo, se genera un mensaje de error. El valor de clasificación no ponderado para un término se multiplica por el valor de peso del término.

Si no se especifica ningún peso para un término de coincidencia, se implica el valor predeterminado, 1,0.

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se aplican pesos a los dos términos de coincidencia de ISABOUT, con la sintaxis Long y Short para los valores de ponderación.


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

 

 



