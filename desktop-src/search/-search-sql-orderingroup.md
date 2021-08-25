---
description: La cláusula ORDER IN GROUP se usa junto con la instrucción GROUP ON, que devuelve conjuntos de resultados en grupos.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: CLÁUSULA ORDER IN GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944657"
---
# <a name="order-in-group-clause"></a>CLÁUSULA ORDER IN GROUP

La cláusula ORDER IN GROUP se usa junto con la [instrucción GROUP ON,](-search-sql-group-on-over.md) que devuelve conjuntos de resultados en grupos. La cláusula ORDER IN GROUP permite ordenar cada grupo devuelto de una manera diferente. Si agrupa en System.Kind, por ejemplo, puede ordenar todos los documentos por System.Document. LastAuthor, todos los archivos de música por sistema. Música. AlbumArtist y todos los correos electrónicos de System.Message.FromName.

## <a name="syntax"></a>Syntax

A continuación se muestra la sintaxis de la cláusula ORDER IN GROUP:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



El especificador de nombre de grupo es un intervalo o un valor conocido de la columna group, tal y como se especifica en la instrucción GROUP ON. Por ejemplo, los valores conocidos de System.Photo.ISOSpeed incluirían "ISO-100", "ISO-200", y así sucesivamente. Un intervalo para System.Photo.DateTaken incluiría "2006-1-1" y "2007-1-1" para una instrucción como GROUP ON System.ItemDate \[ "2006-1-1", "2007-1-1". \]

El especificador de columna debe ser una columna válida especificada en la instrucción GROUP ON o SELECT. Puede incluir más de una columna, separadas por comas. Por ejemplo, si agrupa en System.Photo.ISOSpeed, puede ordenar todas las fotos ISO-100, primero por System.Photo.ApertureSpeed y luego por System.Photo.Aperture.

El especificador de dirección opcional puede ser ASC para ascendente (bajo a alto) o DESC para descendente (de alto a bajo). Si no proporciona un especificador de dirección, se usa el valor predeterminado, ascendente. Si especifica más de una columna, pero no especifica todas las direcciones, la dirección que especifique en último lugar se aplicará a cada columna sucesiva hasta que cambie explícitamente la dirección.

Los intervalos o valores que no se especifican explícitamente en una cláusula ORDER GROUP IN se ordenan en orden ascendente por los valores de la columna GROUP ON.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se agrupan los resultados por la propiedad System.Kind. La consulta ordenaría el grupo "program" por el nombre de la aplicación y el grupo "music" por el título del álbum y el número de pista. El **grupo NULL** se ordenaría por el nombre del elemento. Todos los demás grupos se ordenarían por la fecha del elemento.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



En el ejemplo siguiente se agrupan los resultados por la propiedad System.ItemDate y, a continuación, se ordena cada grupo por dirección URL, tipo o nombre de elemento.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Los resultados de la consulta anterior se devolverían en cinco grupos y se ordenarían como se describe en la tabla siguiente.



| Grupo    | Descripción                                               | Ordenado por                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | Elementos con fechas anteriores al 1-1-2006                          | Ordenado por la dirección URL del elemento, en orden ascendente |
| 2006-1-1 | Elementos con fechas 2006-1-1 o 2006, pero anteriores al 1-1 de 2007 | Ordenado por fecha de elemento, en orden ascendente      |
| 2007-1-1 | Elementos con fechas 2007-1-1 o 2007, pero anteriores al 1-1 de 2008 | Ordenado por valor de tipo, en orden ascendente     |
| 2008-1-1 | Elementos con fechas 2008-1-1 o 2008                     | Ordenado por fecha de elemento, en orden ascendente      |
| **NULL** | Elementos sin valor en la columna System.ItemDate         | Ordenado por nombre de elemento, en orden ascendente      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[GROUP ON ... Sobre... Declaración](-search-sql-group-on-over.md)
</dt> <dt>

[CLÁUSULA ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



