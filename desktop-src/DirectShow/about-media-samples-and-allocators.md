---
description: Acerca de los ejemplos y asignadores de medios
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Acerca de los ejemplos y asignadores de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162473"
---
# <a name="about-media-samples-and-allocators"></a>Acerca de los ejemplos y asignadores de medios

Los filtros entregan datos entre conexiones de pin. Los datos se mueven desde el pin de salida de un filtro al pin de entrada de otro filtro. La manera más común de que el pin de salida entregue los datos es mediante una llamada al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en la entrada, aunque también existen algunos otros mecanismos.

Según el filtro, la memoria de los datos multimedia se puede asignar de varias maneras: en el montón, en una superficie de DirectDraw, mediante memoria GDI compartida o mediante algún otro mecanismo de asignación. El objeto responsable de asignar la memoria se denomina asignador *,* que es un objeto COM que expone la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Cuando se conectan dos pines, uno de ellos debe proporcionar un asignador. DirectShow define una secuencia de llamadas de método que se usa para establecer qué pin proporciona el asignador. Los pines también coinciden en el número de búferes que creará el asignador y en el tamaño de los búferes.

Antes de que comience el streaming, el asignador crea un grupo de búferes. Durante el streaming, el filtro ascendente rellena los búferes con datos y los entrega al filtro de nivel inferior. Pero el filtro ascendente no proporciona punteros sin procesar al filtro de nivel inferior a los búferes. En su lugar, usa objetos COM denominados *ejemplos multimedia*, que el asignador crea para administrar los búferes. Los ejemplos multimedia exponen la [**interfaz IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Un ejemplo multimedia contiene:

-   puntero al búfer subyacente
-   una marca de tiempo
-   varias marcas
-   opcionalmente, un tipo de medio

La marca de tiempo define el tiempo de presentación, que el filtro del representador usa para programar la representación. Las marcas indican cosas como si hubo una interrupción en los datos desde el ejemplo anterior. El tipo de medio proporciona una manera de que los filtros cambien los formatos de la secuencia media. Normalmente, el ejemplo no tiene ningún tipo de medio, lo que indica que el formato no ha cambiado desde el ejemplo anterior.

Mientras un filtro usa un búfer, contiene el recuento de referencias en el ejemplo. El asignador usa el recuento de referencias para determinar cuándo puede volver a usar el búfer. Esto evita que un filtro sobrescriba un búfer que otro filtro sigue usando. Un ejemplo no vuelve al grupo de ejemplos disponibles del asignador hasta que todos los filtros lo han publicado.

Para obtener más información, vea los temas siguientes:

-   En el [tema Ejemplos y asignadores](samples-and-allocators.md) se proporciona una descripción más detallada de cómo funcionan los asignadores.
-   El tema [Data Flow en el filtro Graph](data-flow-in-the-filter-graph.md) proporciona información general sobre el flujo de datos en DirectShow.

Los temas siguientes están destinados a desarrolladores que escriben sus propios filtros personalizados:

-   [Datos Flow para desarrolladores de filtros](data-flow-for-filter-developers.md)
-   [Subprocesos y secciones críticas](threads-and-critical-sections.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El filtro Graph y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



