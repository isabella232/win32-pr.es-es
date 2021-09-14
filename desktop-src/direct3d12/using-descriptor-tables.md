---
title: Uso de las tablas de descriptores
description: Las tablas de descriptores, cada una de las que identifican un intervalo en un montón de descriptores, se enlazan en ranuras definidas por la firma raíz actual en una lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072842"
---
# <a name="using-descriptor-tables"></a>Uso de las tablas de descriptores

Las tablas de descriptores, cada una de las que identifican un intervalo en un montón de descriptores, se enlazan en ranuras definidas por la firma raíz actual en una lista de comandos.

-   [Indexación de tablas descriptores](#indexing-descriptor-tables)
-   [Temas relacionados](#related-topics)

Los sombreadores pueden buscar recursos a los que hacen referencia los descriptores que la tabla de descriptores. Otros enlaces de recursos: los búferes de índice, el búfer de vértices, los búferes de salida de flujo, los destinos de representación y la galería de símbolos de profundidad se realizan directamente en una lista de comandos en lugar de a través de descriptores. En resumen:

Las siguientes referencias de recursos pueden compartir la misma tabla de descriptores y montón:

-   Vistas de recursos de sombreador
-   Vistas de acceso no ordenado
-   Vistas de búfer constante

Las siguientes referencias de recursos deben estar en su propio montón de descriptores:

-   Muestras

Los siguientes recursos no se colocan en tablas o montones de descriptores, sino que se enlazan directamente mediante listas de comandos:

-   Búferes de índices
-   Búferes de vértices
-   Búferes de salida de flujo
-   Destinos de representación
-   Vistas de galería de símbolos de profundidad

## <a name="indexing-descriptor-tables"></a>Indexación de tablas descriptores

Los sombreadores no se pueden indexar dinámicamente entre los límites de la tabla de descriptores desde un sitio de llamada determinado del sombreador. Sin embargo, la selección de un descriptor dentro de una tabla de descriptores se puede indexar dinámicamente en el código del sombreador dentro de intervalos del mismo tipo de descriptor (por ejemplo, la indexación en una región contigua de SRV).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> </dl>

 

 




