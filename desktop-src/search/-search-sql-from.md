---
description: Después de la instrucción SELECT, use la cláusula FROM para especificar dónde buscar documentos coincidentes.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Cláusula FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686622"
---
# <a name="from-clause"></a>Cláusula FROM

Después de la instrucción SELECT, use la cláusula FROM para especificar dónde buscar documentos coincidentes. La siguiente es la sintaxis de la cláusula FROM para una consulta local:


```
FROM [<ComputerName>.]SystemIndex
```



Actualmente, Windows Search solo admite un catálogo, SystemIndex. Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo delante del catálogo y una ruta de acceso UNC (Convención de nomenclatura universal) en el equipo remoto en la cláusula SCOPE o DIRECTORY.

Especifique un ámbito como restricción en la cláusula WHERE, tal como se describe en el tema [ámbito y predicados de directorio](-search-sql-folderdepth.md) .

## <a name="examples"></a>Ejemplos


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



En el segundo de los ejemplos anteriores, la consulta se dirige a un equipo remoto llamado "zarascomputer". Tenga en cuenta que este nombre de equipo aparece en las cláusulas FROM y SCOPE. En el tercer ejemplo, la consulta tiene como destino un nombre de recurso compartido "usuarios" en un servidor denominado "Server" (donde la ruta de acceso UNC sería \\ \\ usuarios del servidor \\ ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Información general de la sintaxis de búsqueda de SQL](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Instrucción SELECT](-search-sql-select.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Predicados de ámbito y directorio](-search-sql-folderdepth.md)
</dt> </dl>

 

 



