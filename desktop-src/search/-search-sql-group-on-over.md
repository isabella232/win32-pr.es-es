---
description: El grupo en...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: AGRUPAR POR... MÁS DE... Privacidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153958"
---
# <a name="group-on--over--statement"></a>AGRUPAR POR... MÁS DE... Privacidad

El grupo en... MÁS de... la instrucción devuelve un conjunto de filas jerárquico en el que los resultados de la búsqueda se dividen en grupos basándose en una columna especificada y en los intervalos de agrupación opcionales. Si agrupa en la columna [System. Kind](../properties/props-system-kind.md) , el conjunto de resultados se divide en varios grupos: uno para los documentos, otro para las comunicaciones, etc. Si agrupa en [System. Size](../properties/props-system-size.md) y group Range 100 KB, el conjunto de resultados se divide en tres grupos: elementos de tamaño < 100 KB, elementos de tamaño >= 100 KB y elementos sin valor de tamaño. También puede Agregar agrupaciones con funciones.

En este tema se tratan los siguientes temas:

-   [Sintaxis](#syntax)
-   [Intervalos de grupo](#group-ranges)
-   [Etiquetar grupos](#labeling-groups)
-   [Ordenar grupos](#ordering-groups)
-   [Anidar grupos](#nesting-groups)
-   [Agrupar en propiedades de vector](#grouping-on-vector-properties)
-   [Más ejemplos](#more-examples)
-   [Temas relacionados](#related-topics)

## <a name="syntax"></a>Sintaxis

El grupo en... MÁS DE... la instrucción tiene la siguiente sintaxis:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



donde los intervalos de agrupación se definen de la manera siguiente:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



El grupo en <column> puede ser un [identificador](-search-sql-identifiers.md) normal o delimitado para una propiedad en el almacén de propiedades.

El opcional <group ranges> es una lista de uno o más valores (número, fecha o cadena) que se usan para dividir los resultados en grupos. <range limit>Identifica un punto de división en el conjunto de resultados devuelto y el <label> identifica una etiqueta descriptiva para un grupo. Puede dividir el conjunto de resultados en tantos grupos como sea necesario.

El primer grupo de resultados incluye elementos con el valor mínimo posible para la propiedad especificada hasta el límite del primer intervalo, sin incluirlo. Se puede hacer referencia a este grupo con la palabra clave MINVALUE. Se puede hacer referencia al segundo grupo con el especificador de límite de intervalo en sí e incluye los elementos cuyo valor de la propiedad especificada es igual o mayor que el límite de intervalo. Los elementos que no tienen un valor para la propiedad especificada se devuelven en último lugar y se puede hacer referencia a ellos con la palabra clave **null** .

Por ejemplo, un límite de intervalo de ' 2006-01-01 ' para la propiedad [System. DateCreated](../properties/props-system-datecreated.md) divide el conjunto de resultados en elementos con fechas anteriores a 2006-01-01 (grupo MINVALUE), elementos con fechas de la 2006-01-01 (grupo de 2006-01-01) y elementos sin fecha (grupo **null** ).

Dentro de cada grupo, los resultados se ordenan por los valores de la columna AGRUPAr por de forma predeterminada. La cláusula [order by](-search-sql-orderby.md) opcional puede contener un especificador de dirección de ASC para ascendente (de menor a mayor) o DESC para descendente (de alto a bajo) y el [orden en la cláusula Group by](-search-sql-orderingroup.md) puede ordenar cada grupo mediante reglas diferentes. Vea la sección [grupos de ordenación](#ordering-groups) a continuación para obtener más información.

## <a name="group-ranges"></a>Intervalos de grupo

En la tabla siguiente se muestra cómo los resultados se dividen en grupos basados en los límites de intervalo:



| Ejemplo ( <column> \[ intervalos de grupo \] )        | Resultado                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System. Size \[ 1000, 5000\]                       | Los resultados se agrupan en cuatro cubos: **MINVALUE**: Size < 1000<br/> **1000:** 1000 <= tamaño < 5000<br/> **5000:** Tamaño >= 5000<br/> **Null:** Ningún valor para el tamaño<br/>                                                                      |
| System. Author \[ before (' m '), After (' r ')\]         | Los resultados se agrupan en cuatro cubos: **MINVALUE:** autor < carácter antes que "m"<br/> **m:** carácter antes de "m" <= autor < carácter después de "r"<br/> **r:** carácter después de "r" <= autor<br/> **Null:** No hay ningún valor para autor<br/>      |
| System. Author \[ MINVALUE/' a to l ', ' m '/i a z '\] | Los resultados se agrupan en tres depósitos: a **a l:** autor < "m"<br/> **de m a z:** "m" <= autor <br/> **Null:** No hay ningún valor para autor<br/>                                                                                                               |
| System. DateCreated \[ ' 2005-1-01 ', ' 2006-6-01 '\]   | Los resultados se agrupan en cuatro cubos:<br/> **MINVALUE:** DateCreated < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **Null:** Ningún valor para DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Errónea `GROUP ON System.Author['m','z','a']`
>
> Correcto `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Etiquetar grupos

Para mejorar la legibilidad, puede etiquetar los grupos con la siguiente sintaxis:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



La etiqueta se separa del límite de intervalo con una marca de barra diagonal y se escribe entre comillas simples. Si no especifica una etiqueta, el nombre de grupo es la cadena de límite de intervalo.

El siguiente es un ejemplo de grupos de etiquetas:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



En Windows 7 o versiones posteriores, también puede usar una \[ etiqueta genérica \] de otro para combinar varios intervalos de agrupación. Los resultados de todos los grupos identificados con esta etiqueta se combinarán en un grupo con esta etiqueta. Este grupo de resultados se devuelve después de todos los demás grupos excepto el grupo **null** . El grupo **null** contiene los resultados de los elementos que no tienen un valor para la propiedad especificada. Antes de Windows 7, la \[ otra \] etiqueta se trata como cualquier otra etiqueta de grupo.

El código siguiente es un ejemplo del uso de la \[ otra \] etiqueta para los grupos que se crearían en Windows 7 o posterior:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



En la tabla siguiente se muestran los grupos que se crearían con el código de agrupación anterior en Windows 7 o posterior.



| Grupo     | System.Author | System. FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Reina         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| Y         | Zara          | amet.docx       |
| \[DISTINTA\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Ordenar grupos

Hay tres maneras de ordenar los elementos de los grupos:

-   Ordenación predeterminada: Si no se especifica lo contrario, los resultados se ordenan por los valores de la columna AGRUPAr por en orden ascendente.
-   ORDER BY: puede especificar el orden descendente en una cláusula ORDER BY. Debe ordenar los resultados por el grupo en la columna.
-   ORDENAR por AGRUPAr por: puede especificar un orden diferente para cada grupo. Si agrupa en [System. Kind](../properties/props-system-kind.md), puede ordenar documentos por System. [Author](../properties/props-system-author.md) y música por [System. Music. artista](../properties/props-system-music-artist.md).

Para obtener más información sobre la ordenación de los resultados, vea las páginas de referencia de cláusula [order by](-search-sql-orderby.md) y [Order in Group](-search-sql-orderingroup.md) .

## <a name="nesting-groups"></a>Anidar grupos

Puede anidar grupos con varias cláusulas GROUP BY. El orden especificado en la consulta se refleja directamente en la jerarquía de grupos de salida, tal y como se muestra en el ejemplo siguiente.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System. Kind    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| perdidos      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| comunicaciones | Abner         | 2006-04-16         |
|                | José          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Agrupar en propiedades de vector

Agrupar en propiedades de Vector, propiedades que pueden contener uno o varios valores simultáneamente, compara los valores de vector individualmente de forma predeterminada. Por ejemplo, si hay un documento, Lorem.docx, con la propiedad System. Author como "Theresa;" Zara "y otro documento, Ipsum.docx, con la propiedad System. Author como" Zara ", la consulta devuelve el conjunto de resultados en dos grupos, como se muestra aquí:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System. FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Como puede ver, la agrupación en propiedades de vector devuelve filas duplicadas. Lorem.docx aparece dos veces porque tiene dos autores.

 

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

[Cláusula ORDER BY](-search-sql-orderby.md)
</dt> <dt>

[ORDER IN GROUP (cláusula)](-search-sql-orderingroup.md)
</dt> </dl>

 

 
