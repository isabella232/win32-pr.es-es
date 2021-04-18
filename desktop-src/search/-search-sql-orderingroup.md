---
description: La cláusula ORDER IN GROUP se utiliza junto con la instrucción GROUP ON, que devuelve conjuntos de resultados en grupos.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER IN GROUP (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360189"
---
# <a name="order-in-group-clause"></a>ORDER IN GROUP (cláusula)

La cláusula ORDER IN GROUP se utiliza junto con la instrucción [Group on](-search-sql-group-on-over.md) , que devuelve conjuntos de resultados en grupos. La cláusula ORDER IN GROUP permite ordenar cada grupo devuelto de manera diferente. Si agrupa en System. Kind, por ejemplo, puede ordenar todos los documentos por System.Document. LastAuthor, todos los archivos de música por System. Music. AlbumArtist y todos los mensajes de correo electrónico por System. Message. FromName.

## <a name="syntax"></a>Sintaxis

La siguiente es la sintaxis de la cláusula ORDER en GROUP:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



El especificador de nombre de grupo es un intervalo o un valor conocido de la columna Group, tal como se especifica en la instrucción GROUP ON. Por ejemplo, los valores conocidos de System. Photo. isospeed incluirían ' ISO-100 ', ' ISO-200 ', etc. Un intervalo para System. Photo. DateTaken incluiría ' 2006-1-1 ' y ' 2007-1-1 ' para una instrucción como GROUP ON System. ItemDate \[ ' 2006-1-1 ', ' 2007-1-1 ' \] .

El especificador de columna debe ser una columna válida especificada en el grupo en o en la instrucción SELECT. Puede incluir más de una columna, separadas por comas. Por ejemplo, si agrupa en System. Photo. isospeed, puede ordenar todas las fotos de ISO-100, primero por System. Photo. ShutterSpeed y, a continuación, por System. Photo. abertura.

El especificador de dirección opcional puede ser ASC para ascendente (de menor a mayor) o DESC para descendente (de alto a bajo). Si no se proporciona un especificador de dirección, se utiliza el valor predeterminado, ascendente. Si especifica más de una columna, pero no especifica todas las direcciones, la dirección que especifique en último lugar se aplicará a cada columna sucesiva hasta que cambie explícitamente la dirección.

Los intervalos o valores que no se especifican explícitamente en una cláusula ORDER GROUP IN se ordenan en orden ascendente por los valores de la columna GROUP ON.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se agrupan los resultados por la propiedad System. Kind. La consulta ordenaría el grupo ' Program ' por el nombre de la aplicación y el grupo ' Music ' por el título del álbum y el número de seguimiento. El grupo **null** se ordenará por el nombre del elemento. Todos los demás grupos ordenarían por la fecha del elemento.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



En el ejemplo siguiente se agrupan los resultados por la propiedad System. ItemDate y, a continuación, se ordenan cada grupo por dirección URL, tipo o nombre de elemento.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Los resultados de la consulta anterior se devolverían en cinco grupos y se ordenarían según se describe en la tabla siguiente.



| Grupo    | Descripción                                               | Ordenado por                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | Elementos con fechas anteriores a 2006-1-1                          | Ordenados por dirección URL del elemento, en orden ascendente |
| 2006-1-1 | Elementos con fechas de la 2006-1-1, pero anteriores a 2007-1-1 | Ordenados por fecha de elemento, en orden ascendente      |
| 2007-1-1 | Elementos con fechas de la 2007-1-1, pero anteriores a 2008-1-1 | Ordenado por valor de tipo, en orden ascendente     |
| 2008-1-1 | Elementos con fechas en o después de 2008-1-1                     | Ordenados por fecha de elemento, en orden ascendente      |
| **NULL** | Elementos sin valor en la columna System. ItemDate         | Ordenado por nombre de elemento, en orden ascendente      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[AGRUPAR POR... MÁS de... Privacidad](-search-sql-group-on-over.md)
</dt> <dt>

[Cláusula ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



