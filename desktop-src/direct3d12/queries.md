---
title: Consultas
description: En Direct3D 12, las consultas se agrupan en matrices de consultas denominadas montón de consultas. Un montón de consultas tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241955"
---
# <a name="queries"></a>Consultas

En Direct3D 12, las consultas se agrupan en matrices de consultas denominadas montón de consultas. Un montón de consultas tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.

-   [Diferencias en las consultas de Direct3D 11 a Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Montones de consulta](#query-heaps)
-   [Creación de montones de consulta](#creating-query-heaps)
-   [Extracción de datos de una consulta](#extracting-data-from-a-query)
-   [Temas relacionados](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Diferencias en las consultas de Direct3D 11 a Direct3D 12

Los siguientes tipos de consulta ya no están presentes en Direct3D 12 y su funcionalidad se incorpora a otros procesos:

-   **Consultas de eventos:** el evento se controla funcionalmente mediante barreras.
-   **Consultas de marca de tiempo** desconexas: los relojes de GPU se pueden establecer en un estado estable en Direct3D 12 (consulte la [sección Control de](timing.md) tiempo). Las comparaciones de reloj de GPU no son significativas si la GPU está inactiva en absoluto entre las marcas de tiempo (conocidas como consulta no ungida). Con una potencia estable, las consultas de marca de tiempo de dos emitidas desde diferentes listas de comandos son comparables de forma confiable. Dos marcas de tiempo dentro de la misma lista de comandos siempre son comparables de forma confiable.
-   **Consultas de estadísticas de salida de** flujo: en Direct3D 12 no hay ninguna consulta de desbordamiento de salida de secuencia única (SO) para todos los flujos de salida. Las aplicaciones deben emitir varias consultas de secuencia única y, a continuación, correlacionar los resultados.
-   Consultas de predicado de estadísticas de salida de flujo y predicado de **oclusión:** las consultas (que escriben en memoria) y [predicación](predication.md) (que lee de la memoria) ya no están acopladas, por lo que estos tipos de consulta no son necesarios.

Se ha agregado un nuevo tipo de consulta de oclusión binaria a Direct3D 12. Esto permite que las estrategias de predicado que solo se ocupan de si un objeto se oclusó completamente o no (en lugar de cuántos píxeles se han ocluido) indiquen esto al dispositivo, lo que podría ser capaz de realizar las consultas de forma más eficaz.

## <a name="query-heaps"></a>Montones de consultas

Las consultas pueden ser de varios tipos [**(D3D12 \_ QUERY \_ HEAP \_ TYPE)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)y se agrupan en montones de consultas antes de enviarse a la GPU.

Hay disponible un nuevo tipo de consulta D3D12 QUERY TYPE BINARY OCCLUSION que actúa como \_ \_ D3D12 QUERY TYPE OCCLUSION, salvo que devuelve un resultado binario de \_ \_ \_ \_ \_ 0/1: 0 indica que ninguna muestra pasó pruebas de profundidad y galería de símbolos, 1 indica que al menos una muestra pasó pruebas de profundidad y galería de símbolos. Esto permite que las consultas de oclusión no interfieran con ninguna optimización del rendimiento de GPU asociada a las pruebas de profundidad o galería de símbolos.

## <a name="creating-query-heaps"></a>Creación de montones de consulta

Las API pertinentes para crear montones de consultas son la enumeración [**D3D12 \_ QUERY \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type), la estructura [**D3D12 \_ QUERY \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)y el [**método CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

El entorno de ejecución principal validará que el tipo de montón de consulta es un miembro válido de la enumeración [**D3D12 \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) y que el recuento es mayor que 0.

Cada elemento de consulta individual dentro de un montón de consultas se puede iniciar y detener por separado.

Las API para usar los montones de consulta son la enumeración [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)y los métodos [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) [**y EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

D3D12 \_ QUERY TYPE TIMESTAMP es la única consulta que solo admite \_ \_ [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) Todos los demás tipos de consulta [**requieren BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) **y EndQuery.**

La capa de depuración validará lo siguiente:

-   No es posible iniciar una consulta de marca de &mdash; tiempo que solo se puede finalizar.
-   No es posible iniciar una consulta dos veces sin finalizarla (para un elemento determinado). Para las consultas que requieren tanto el inicio como el final, no es posible finalizar una consulta antes del inicio correspondiente (para un elemento determinado).
-   El tipo de consulta pasado [**a BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) debe coincidir con el tipo de consulta pasado [**a EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

El entorno de ejecución principal validará lo siguiente:

-   [**No se puede llamar**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) a BeginQuery en una consulta de marca de tiempo.
-   Para los tipos de consulta que [**admiten BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (todos excepto la marca de tiempo), una consulta para un elemento determinado no debe abarcar los límites de la lista de comandos.
-   *ElementIndex* debe estar dentro del intervalo.
-   El tipo de consulta es un miembro válido de la [**enumeración \_ QUERY TYPE \_ de D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)
-   El tipo de consulta debe ser compatible con el montón de consultas. En la tabla siguiente se muestra el tipo de montón de consultas necesario para cada tipo de consulta:

    

    | Tipo de consulta                                  | Tipo de montón de consulta                                |
    |---------------------------------------------|------------------------------------------------|
    | OCLUSIÓN DEL TIPO DE CONSULTA D3D12 \_ \_ \_               | OCLUSIÓN DEL TIPO \_ \_ DE MONTÓN DE CONSULTA \_ D3D12 \_            |
    | OCLUSIÓN BINARIA DEL TIPO \_ \_ DE CONSULTA \_ D3D12 \_       | OCLUSIÓN DEL TIPO \_ \_ DE MONTÓN DE CONSULTA \_ D3D12 \_            |
    | MARCA DE TIEMPO DEL TIPO DE CONSULTA D3D12 \_ \_ \_               | MARCA DE TIEMPO DEL TIPO DE \_ \_ MONTÓN DE CONSULTA \_ D3D12 \_            |
    | ESTADÍSTICAS DE CANALIZACIÓN DEL TIPO DE CONSULTA D3D12 \_ \_ \_ \_    | ESTADÍSTICAS DE CANALIZACIÓN DEL TIPO \_ \_ DE MONTÓN DE \_ \_ CONSULTAS D3D12 \_ |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM0 | TIPO DE MONTÓN DE CONSULTA D3D12 \_ \_ SO \_ \_ \_ STATISTICS       |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM1 | TIPO DE MONTÓN DE CONSULTA D3D12 \_ \_ SO \_ \_ \_ STATISTICS       |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM2 | TIPO DE MONTÓN DE CONSULTA D3D12 \_ \_ SO \_ \_ \_ STATISTICS       |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM3 | TIPO DE MONTÓN DE CONSULTA D3D12 \_ \_ SO \_ \_ \_ STATISTICS       |

    

     

-   El tipo de consulta es compatible con el tipo de lista de comandos. En la tabla siguiente se muestran las consultas que se admiten en qué tipos de lista de comandos.

    

    | Tipo de consulta                                  | Tipos de lista de comandos admitidos         |
    |---------------------------------------------|--------------------------------------|
    | OCLUSIÓN DEL TIPO DE CONSULTA D3D12 \_ \_ \_               | Directo                               |
    | OCLUSIÓN BINARIA DEL TIPO \_ \_ DE CONSULTA \_ D3D12 \_       | Directo                               |
    | MARCA DE TIEMPO DEL TIPO DE CONSULTA D3D12 \_ \_ \_               | Direct, Compute y, opcionalmente, Copy |
    | ESTADÍSTICAS DE CANALIZACIÓN DEL TIPO DE CONSULTA D3D12 \_ \_ \_ \_    | Directo                               |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM0 | Directo                               |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM1 | Directo                               |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM2 | Directo                               |
    | TIPO DE CONSULTA D3D12 \_ \_ SO \_ \_ STATISTICS \_ STREAM3 | Directo                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extracción de datos de una consulta

La manera de extraer datos de una consulta es usar el [**método ResolveQueryData.**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) **ResolveQueryData funciona** con todos los tipos de memoria (ya sean memoria del sistema o memoria local del dispositivo), pero requiere que el recurso de destino esté [**en D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). 

## <a name="related-topics"></a>Temas relacionados

* [Contadores y consultas](counters-and-queries.md)
* [Paso a paso de consultas de predicado](predication-queries.md)
