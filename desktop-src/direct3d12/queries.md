---
title: Consultas
description: En Direct3D 12, las consultas se agrupan en matrices de consultas llamadas un montón de consultas. Un montón de consulta tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c4db895eb0d4a727db2e32757f7ab0f1f9b1e2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104549155"
---
# <a name="queries"></a>Consultas

En Direct3D 12, las consultas se agrupan en matrices de consultas llamadas un montón de consultas. Un montón de consulta tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.

-   [Diferencias en las consultas de Direct3D 11 a Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Montones de consultas](#query-heaps)
-   [Crear montones de consulta](#creating-query-heaps)
-   [Extraer datos de una consulta](#extracting-data-from-a-query)
-   [Temas relacionados](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Diferencias en las consultas de Direct3D 11 a Direct3D 12

Los siguientes tipos de consulta ya no están presentes en Direct3D 12, su funcionalidad se incorpora a otros procesos:

-   **Consultas de eventos** : el evento se controla ahora mediante barreras.
-   Consultas de marca de tiempo no **contiguas** : los relojes de GPU se pueden establecer en un estado estable en Direct3D 12 (consulte la sección de [temporización](timing.md) ). Las comparaciones del reloj de GPU no son significativas si la GPU está inactiva en todas las marcas de tiempo (lo que se conoce como consulta no conjunta). Con la potencia estable dos consultas de marca de tiempo emitidas desde distintas listas de comandos son comparables de forma confiable. Dos marcas de tiempo dentro de la misma lista de comandos siempre son comparables de forma confiable.
-   **Consultas de estadísticas de salida de flujo** : en Direct3D 12 no hay ninguna consulta de desbordamiento de salida de flujo único (SO) para todos los flujos de salida. Las aplicaciones deben emitir varias consultas de un solo flujo y, a continuación, correlacionar los resultados.
-   **Las consultas de predicado de salida de flujo y las consultas de predicado de oclusión** : las consultas (que escriben en memoria) y [Predication](predication.md) (que lee de la memoria) ya no están acopladas, por lo que estos tipos de consulta no son necesarios.

Se ha agregado un nuevo tipo de consulta de oclusión binaria a Direct3D 12. Esto permite que las estrategias de predication que se requieran solo que un objeto sea totalmente ocluidos o no (en lugar de cuántos píxeles se ocluidos) para indicarlo al dispositivo, lo que podría ser capaz de realizar las consultas de forma más eficaz.

## <a name="query-heaps"></a>Montones de consultas

Las consultas pueden ser una de una serie de tipos ([**D3D12 \_ query \_ heap \_ Type**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) y se agrupan en montones de consulta antes de enviarse a la GPU.

Hay disponible un nuevo tipo de consulta D3D12 de tipo de consulta " \_ \_ \_ oclusión binaria" \_ y actúa como \_ el tipo de consulta D3D12 \_ \_ oclusión, con la salvedad de que devuelve un resultado binario 0/1:0 indica que no se han superado las pruebas de profundidad y de estarcido, 1 indica que al menos una muestra de profundidad y de estarcido superada. Esto permite que las consultas de oclusión no interfieran con ninguna optimización de rendimiento de GPU asociada a las pruebas de profundidad y estarcido.

## <a name="creating-query-heaps"></a>Crear montones de consulta

Las API relacionadas con la creación de montones de consulta son [**el \_ \_ \_ tipo de montón de consulta**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)de enumeración D3D12, la [**\_ \_ \_ Descripción del montón de consulta**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)de struct D3D12 y el método [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

El tiempo de ejecución principal validará que el tipo de montón de consulta sea un miembro válido de la enumeración de [**\_ \_ tipo de montón D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) y que el recuento sea mayor que 0.

Cada elemento de consulta individual dentro de un montón de consulta se puede iniciar y detener por separado.

Las API para usar los montones de consulta son el [**tipo de \_ consulta \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)de enumeración y los métodos [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

\_ \_ \_ La marca de tiempo de tipo de consulta D3D12 es la única consulta que solo admite [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) . Todos los demás tipos de consulta requieren [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y **EndQuery**.

El nivel de depuración validará lo siguiente:

-   No se puede iniciar una consulta de marca de tiempo &mdash; que solo se pueda finalizar
-   No es válido iniciar una consulta dos veces sin terminarla (para un elemento determinado). En el caso de las consultas que requieren Begin y end, no es válido finalizar una consulta antes del Begin correspondiente (para un elemento determinado).
-   El tipo de consulta que se pasa a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) debe coincidir con el tipo de consulta pasado a [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

El entorno de tiempo de ejecución principal validará lo siguiente:

-   No se puede llamar a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) en una consulta de marca de tiempo.
-   En el caso de los tipos de consulta que admiten [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (todos excepto para la marca de tiempo), una consulta para un elemento determinado no debe abarcar los límites de la lista de comandos.
-   *ElementIndex* debe estar dentro del intervalo.
-   El tipo de consulta es un miembro válido de la enumeración de [**\_ \_ tipo de consulta D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) .
-   El tipo de consulta debe ser compatible con el montón de consultas. En la tabla siguiente se muestra el tipo de montón de consulta necesario para cada tipo de consulta:

    

    | Tipo de consulta                                  | Tipo de montón de consulta                                |
    |---------------------------------------------|------------------------------------------------|
    | \_Tipo de consulta D3D12 \_ \_ oclusión               | \_Tipo de montón de consulta D3D12 \_ \_ \_ oclusión            |
    | \_Tipo de consulta D3D12 \_ \_ oclusión binaria \_       | \_Tipo de montón de consulta D3D12 \_ \_ \_ oclusión            |
    | Marca de tiempo de \_ tipo de consulta D3D12 \_ \_               | Marca de tiempo de tipo de montón de \_ consulta D3D12 \_ \_ \_            |
    | \_Estadísticas de \_ \_ canalización de tipo de consulta D3D12 \_    | D3D12 \_ \_ estadísticas de \_ \_ canalización de tipo de montón de consulta \_ |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM0 | \_Tipo de montón de consulta D3D12 \_ \_ \_ para \_ estadísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM1 | \_Tipo de montón de consulta D3D12 \_ \_ \_ para \_ estadísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM2 | \_Tipo de montón de consulta D3D12 \_ \_ \_ para \_ estadísticas       |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM3 | \_Tipo de montón de consulta D3D12 \_ \_ \_ para \_ estadísticas       |

    

     

-   El tipo de consulta es compatible con el tipo de lista de comandos. En la tabla siguiente se muestran las consultas que se admiten en cada tipo de lista de comandos.

    

    | Tipo de consulta                                  | Tipos de lista de comandos admitidos         |
    |---------------------------------------------|--------------------------------------|
    | \_Tipo de consulta D3D12 \_ \_ oclusión               | Directo                               |
    | \_Tipo de consulta D3D12 \_ \_ oclusión binaria \_       | Directo                               |
    | Marca de tiempo de \_ tipo de consulta D3D12 \_ \_               | Direct, Compute y opcionalmente copia |
    | \_Estadísticas de \_ \_ canalización de tipo de consulta D3D12 \_    | Directo                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM0 | Directo                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM1 | Directo                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM2 | Directo                               |
    | \_Tipo de consulta D3D12 \_ \_ para \_ estadísticas \_ STREAM3 | Directo                               |

    

     

## <a name="extracting-data-from-a-query"></a>Extraer datos de una consulta

La manera de extraer los datos de una consulta es usar el método [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) . **ResolveQueryData** funciona con todos los tipos de memoria (tanto si son de memoria del sistema como de memoria local del dispositivo), pero requiere que el recurso de destino esté en [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). 

## <a name="related-topics"></a>Temas relacionados

* [Contadores y consultas](counters-and-queries.md)
* [Tutoriales de consultas de Predication](predication-queries.md)
