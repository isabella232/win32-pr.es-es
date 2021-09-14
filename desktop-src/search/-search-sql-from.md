---
description: Después de la instrucción SELECT, se usa la cláusula FROM para especificar dónde buscar documentos que coincidan.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: From (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363214"
---
# <a name="from-clause"></a>From (cláusula)

Después de la instrucción SELECT, se usa la cláusula FROM para especificar dónde buscar documentos que coincidan. A continuación se muestra la sintaxis de la cláusula FROM para una consulta local:


```
FROM [<ComputerName>.]SystemIndex
```



Actualmente, Windows Search solo admite un catálogo, SystemIndex. Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo antes del catálogo y una ruta de acceso de convención de nomenclatura universal (UNC) en el equipo remoto en la cláusula SCOPE o DIRECTORY.

Especifique un ámbito como restricción en la cláusula WHERE, como se describe en el [tema SCOPE y DIRECTORY Predicates.](-search-sql-folderdepth.md)

## <a name="examples"></a>Ejemplos


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



En el segundo de los ejemplos anteriores, la consulta tiene como destino un equipo remoto denominado "equipo informático". Observe que este nombre de equipo aparece en las cláusulas FROM y SCOPE. En el tercer ejemplo, la consulta tiene como destino un nombre de recurso compartido "usuarios" en un servidor denominado "servidor" (donde la ruta de acceso UNC serían usuarios \\ \\ del \\ servidor).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Información general sobre la sintaxis de SQL búsqueda](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Instrucción SELECT](-search-sql-select.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Predicados SCOPE y DIRECTORY](-search-sql-folderdepth.md)
</dt> </dl>

 

 



