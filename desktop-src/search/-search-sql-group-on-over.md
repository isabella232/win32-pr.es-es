---
description: The GROUP ON...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: GROUP ON ... SOBRE... Declaración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882016"
---
# <a name="group-on--over--statement"></a>GROUP ON ... SOBRE... Declaración

The GROUP ON... SOBRE... la instrucción devuelve un conjunto de filas jerárquico en el que los resultados de la búsqueda se dividen en grupos en función de una columna especificada y de intervalos de agrupación opcionales. Si agrupa en la [columna System.Kind,](../properties/props-system-kind.md) el conjunto de resultados se divide en varios grupos: uno para documentos, otro para comunicaciones, y así sucesivamente. Si agrupa en [System.Size](../properties/props-system-size.md) y el intervalo de grupos de 100 KB, el conjunto de resultados se divide en tres grupos: elementos de tamaño < 100 KB, elementos de tamaño >= 100 KB y elementos sin valor de tamaño. También puede agregar agrupaciones con funciones.

En este tema se tratan los temas siguientes:

-   [Sintaxis](#syntax)
-   [Intervalos de grupo](#group-ranges)
-   [Etiquetado de grupos](#labeling-groups)
-   [Ordenación de grupos](#ordering-groups)
-   [Anidamiento de grupos](#nesting-groups)
-   [Agrupación en propiedades vectoriales](#grouping-on-vector-properties)
-   [Más ejemplos](#more-examples)
-   [Temas relacionados](#related-topics)

## <a name="syntax"></a>Syntax

GROUP ON ... SOBRE... la instrucción tiene la sintaxis siguiente:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



donde los intervalos de agrupación se definen de la siguiente manera:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



La columna GROUP ON &lt; puede ser un identificador normal o &gt; [delimitado](-search-sql-identifiers.md) para una propiedad en el almacén de propiedades.

El opcional es una lista de uno o varios valores (número, fecha o cadena) que se usan para <group ranges> dividir los resultados en grupos. identifica un punto de división en el conjunto de resultados devuelto y identifica <range limit> una etiqueta fácil de usar para un <label> grupo. Puede dividir el conjunto de resultados en tantos grupos como necesite.

El primer grupo de resultados incluye elementos con el valor mínimo posible para la propiedad especificada hasta, pero sin incluir el primer límite de intervalo. Se puede hacer referencia a este grupo con la palabra clave MINVALUE. Se puede hacer referencia al segundo grupo con el propio especificador de límite de intervalo e incluye elementos cuyo valor para la propiedad especificada es igual o mayor que el límite de intervalo. Los elementos que no tienen un valor para la propiedad especificada se devuelven en último lugar y se puede hacer referencia a ellos con la **palabra clave NULL.**

Por ejemplo, un límite de intervalo de "2006-01-01" para la propiedad [System.DateCreated](../properties/props-system-datecreated.md) divide el conjunto de resultados en elementos con fechas anteriores a 2006-01-01 (grupo MINVALUE), elementos con fechas 2006-01-01 (grupo 2006-01-01) y elementos sin fecha (grupo **NULL).**

Dentro de cada grupo, los resultados se ordenan por los valores de la columna GROUP ON de forma predeterminada. La cláusula [ORDER BY](-search-sql-orderby.md) opcional puede contener un especificador de dirección de ASC para ascendente (bajo a alto) o DESC para descendente (alto a bajo), y la cláusula ORDER IN [GROUP BY](-search-sql-orderingroup.md) puede ordenar cada grupo mediante reglas diferentes. Consulte la sección [Grupos de](#ordering-groups) pedidos a continuación para obtener más información.

## <a name="group-ranges"></a>Intervalos de grupo

En la tabla siguiente se muestra cómo se dividen los resultados en grupos en función de los límites de intervalo:



| Ejemplo ( &lt; &gt; \[ intervalos de grupos de columnas \] )        | Resultado                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System.Size \[ 1000, 5000\]                       | Los resultados se agrupan en cuatro cubos: **MINVALUE:** tamaño < 1000<br/> **1000:** 1000 <= Tamaño < 5000<br/> **5000:** Tamaño >= 5000<br/> **NULL:** No hay ningún valor para Tamaño<br/>                                                                      |
| System.Author \[ BEFORE('m'),AFTER('r')\]         | Los resultados se agrupan en cuatro cubos: **MINVALUE:** Author < character before "m"<br/> **m:** carácter antes de "m" <= Autor < después de "r"<br/> **r:** carácter después de "r" <= Autor<br/> **NULL:** No hay ningún valor para Author<br/>      |
| System.Author \[ MINVALUE/'a to l',"m"/'m to z'\] | Los resultados se agrupan en tres depósitos: **a a l:** Author < "m"<br/> **m a z:** "m" <= Author <br/> **NULL:** No hay ningún valor para Author<br/>                                                                                                               |
| System.DateCreated \[ '2005-1-01','2006-6-01'\]   | Los resultados se agrupan en cuatro depósitos:<br/> **MINVALUE:** FechaCreada < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= FechaCreada < 2006-6-01<br/> **1-01-2006:** DateCreated >= 2006-6-01<br/> **NULL:** No hay ningún valor para DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Incorrecta: `GROUP ON System.Author['m','z','a']`
>
> Correcto: `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Etiquetado de grupos

Para mejorar la legibilidad, puede etiquetar grupos mediante la sintaxis siguiente:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



La etiqueta está separada del límite de intervalo con una barra diagonal y se incluye entre comillas simples. Si no especifica una etiqueta, el nombre del grupo es la cadena de límite de intervalo.

A continuación se muestra un ejemplo de etiquetado de grupos:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



En Windows 7 o posterior, también puede usar una etiqueta \[ GENÉRICA OTHER para combinar varios \] intervalos de agrupación. Los resultados de todos los grupos identificados con esta etiqueta se combinarán en un grupo con esta etiqueta. Este grupo de resultados se devuelve después de todos los demás grupos, excepto el **grupo NULL.** El **grupo NULL** contiene los resultados de los elementos que no tienen un valor para la propiedad especificada. Antes de Windows 7, la \[ etiqueta OTHER se trata como cualquier otra etiqueta de \] grupo.

El código siguiente es un ejemplo del uso de la etiqueta OTHER para los grupos que se \[ \] crearían en Windows 7 o posterior:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



En la tabla siguiente se muestran los grupos que crearía el código de agrupación anterior en Windows 7 o posterior.



| Grupo     | System.Author | System.FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Reina         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| S         | Zara          | amet.docx       |
| \[OTRO\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Ordenación de grupos

Hay tres maneras de ordenar elementos en grupos:

-   Ordenación predeterminada: si no especifica lo contrario, los resultados se ordenan por los valores de la columna GROUP ON, en orden ascendente.
-   ORDER BY: puede especificar el orden descendente en una cláusula ORDER BY. Debe ordenar los resultados por la columna GROUP ON.
-   ORDER IN GROUP BY: puede especificar un orden diferente para cada grupo. Si agrupa en [System.Kind](../properties/props-system-kind.md), puede pedir documentos por [System.Author](../properties/props-system-author.md) y música por [System.Música. Artist](../properties/props-system-music-artist.md).

Para obtener más información sobre cómo ordenar los resultados, vea las páginas de referencia [cláusula ORDER BY](-search-sql-orderby.md) y ORDER IN GROUP [Clause.](-search-sql-orderingroup.md)

## <a name="nesting-groups"></a>Anidamiento de grupos

Puede anidar grupos con varias cláusulas GROUP ON. El orden especificado en la consulta se refleja directamente en la jerarquía del grupo de salida, como se muestra en el ejemplo siguiente.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System.Kind    | System.Author | System.DateCreated |
|----------------|---------------|--------------------|
| Documentos      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| comunicaciones | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Agrupación en propiedades vectoriales

La agrupación en propiedades vectoriales, propiedades que pueden contener uno o varios valores simultáneamente, compara los valores vectoriales individualmente de forma predeterminada. Por ejemplo, si hay un documento, Lorem.docx, con la propiedad System.Author como "Theresa; Así como otro documento, Ipsum.docx, con la propiedad System.Author como "Tado", la consulta devuelve el conjunto de resultados en dos grupos, como se muestra aquí:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System.FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Como puede ver, la agrupación en propiedades vectoriales devuelve filas duplicadas. Lorem.docx aparece dos veces porque tiene dos autores.

 

## <a name="more-examples"></a>Más ejemplos


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de agregado](-search-sql-aggregates.md)
</dt> <dt>

[CLÁUSULA ORDER BY](-search-sql-orderby.md)
</dt> <dt>

[CLÁUSULA ORDER IN GROUP](-search-sql-orderingroup.md)
</dt> </dl>

 

 
