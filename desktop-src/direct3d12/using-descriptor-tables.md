---
title: Usar tablas de descriptores
description: Las tablas de descriptores, cada una de las cuales identifican un intervalo en un montón de descriptores, se enlazan en las ranuras definidas por la firma raíz actual en una lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103667"
---
# <a name="using-descriptor-tables"></a>Usar tablas de descriptores

Las tablas de descriptores, cada una de las cuales identifican un intervalo en un montón de descriptores, se enlazan en las ranuras definidas por la firma raíz actual en una lista de comandos.

-   [Indexación de tablas de descriptor](#indexing-descriptor-tables)
-   [Temas relacionados](#related-topics)

Los sombreadores pueden buscar recursos a los que hacen referencia los descriptores que componen la tabla de descriptores. Otros enlaces de recursos: los búferes de índice, el búfer de vértices, los búferes de salida de secuencias, los destinos de representación y la galería de símbolos de profundidad se realizan directamente en una lista de comandos, en lugar de hacerlo a través de descriptores. En resumen:

Las referencias de recursos siguientes pueden compartir la misma tabla de descriptores y el montón:

-   Vistas de recursos del sombreador
-   Vistas de acceso desordenado
-   Vistas de búfer de constantes

Las siguientes referencias de recursos deben estar en su propio montón de descriptores:

-   Muestras

Los siguientes recursos no se colocan en tablas o montones de descriptores, pero se enlazan directamente mediante listas de comandos:

-   Búferes de índices
-   Búferes de vértices
-   Búferes de salida de flujo
-   Destinos de representación
-   Vistas de estarcido de profundidad

## <a name="indexing-descriptor-tables"></a>Indexación de tablas de descriptor

Los sombreadores no pueden indexar dinámicamente los límites de la tabla de descriptores de un sitio de llamada dado en el sombreador. Sin embargo, la selección de un descriptor dentro de una tabla de descriptores puede indexarse dinámicamente en el código del sombreador dentro de los intervalos del mismo tipo de descriptor (por ejemplo, la indexación en una región contigua de SRVs).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> </dl>

 

 




