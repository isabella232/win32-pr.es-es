---
description: Una vez que se devuelve un resultado de una consulta, puede tener acceso a varias propiedades del conjunto de filas.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Propiedades del conjunto de filas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705476"
---
# <a name="rowset-properties"></a>Propiedades del conjunto de filas

Una vez que se devuelve un resultado de una consulta, puede tener acceso a varias propiedades del conjunto de filas.

Además de las propiedades de conjunto de filas estándar de OLE-DB, Windows Search SQL ofrece las cuatro propiedades personalizadas siguientes. El GUID de este conjunto de propiedades es {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.

Windows Search admite la propiedad de OLE DB estándar DBPROP \_ COMMANDTIMEOUT del conjunto de propiedades de conjunto de [ \_ filas DBPROPSET](/previous-versions//ms691738(v=vs.85)) .



| Nombre de propiedad                  | PROPID/Type | Descripción                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | 15/VT \_ bool | Si se establece en true, se evita que se calculen propiedades costosas como los resultados encontrados y el rango máximo que requieren evaluar toda la consulta cuando se tiene acceso a cualquier propiedad de conjunto de filas.                                                                                                                                                                         |
| Rango máximo ( \_ rango máximo)       | 6/VT \_ I4    | La clasificación más alta calculada para cualquier resultado.                                                                                                                                                                                                                                                                                                          |
| Resultados encontrados (resultados \_ encontrados) | 7/VT \_ I4    | Número total de elementos únicos de esta consulta. En el caso de una consulta SELECT, es el número de elementos del conjunto de filas. Para un grupo en consulta, es el número de elementos hoja únicos. Esta propiedad no identifica el número de filas del conjunto de filas de nivel superior (el número de grupos de nivel superior).                                                        |
| Where ID (WHEREID)             | 8/VT \_ I4    | Identificador de las restricciones usadas para una consulta. Si un conjunto de filas está abierto cuando se ejecuta una nueva consulta, la nueva consulta puede volver a usar las restricciones de la consulta anterior, con lo que se aprovecha el trabajo ya completado. Para obtener más información sobre cómo reutilizar las restricciones WHERE, consulte la [función ReuseWhere](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexación de los eventos de priorización y de conjunto de filas en Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
