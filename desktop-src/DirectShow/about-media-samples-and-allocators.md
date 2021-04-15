---
description: Acerca de los ejemplos y asignadores de medios
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Acerca de los ejemplos y asignadores de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689623"
---
# <a name="about-media-samples-and-allocators"></a>Acerca de los ejemplos y asignadores de medios

Los filtros entregan datos a través de conexiones de PIN. Los datos se mueven desde el terminal de salida de un filtro hasta el PIN de entrada de otro filtro. La forma más común de que el PIN de salida entregue los datos es mediante una llamada al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en la entrada, aunque también existen algunos mecanismos.

Dependiendo del filtro, la memoria de los datos multimedia se puede asignar de varias maneras: en el montón, en una superficie de DirectDraw, utilizando la memoria de GDI compartida o usando algún otro mecanismo de asignación. El objeto responsable de la asignación de la memoria se denomina *allocator*, que es un objeto com que expone la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Cuando dos patillas se conectan, uno de los pin debe proporcionar un asignador. DirectShow define una secuencia de llamadas de método que se usa para establecer qué PIN proporciona el asignador. Los pin también aceptan el número de búferes que va a crear el asignador y el tamaño de los búferes.

Antes de que comience el streaming, el asignador crea un grupo de búferes. Durante el streaming, el filtro de nivel superior rellena los búferes con datos y los entrega al filtro de bajada. Pero el filtro de nivel superior no proporciona los punteros sin formato de filtro de bajada a los búferes. En su lugar, utiliza objetos COM denominados *ejemplos de medios*, que el asignador crea para administrar los búferes. Los ejemplos de medios exponen la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Un ejemplo multimedia contiene:

-   puntero al búfer subyacente.
-   una marca de tiempo
-   varias marcas
-   Opcionalmente, un tipo de medio

La marca de tiempo define el tiempo de presentación, que el filtro de representador utiliza para programar la representación. Las marcas indican aspectos como si hubiera una interrupción en los datos desde el ejemplo anterior. El tipo de medio proporciona una manera de que los filtros cambien los formatos a la secuencia intermedia. Normalmente, el ejemplo no tiene ningún tipo de medio, lo que indica que el formato no ha cambiado desde el ejemplo anterior.

Mientras un filtro está utilizando un búfer, contiene el recuento de referencias en el ejemplo. El asignador utiliza el recuento de referencias para determinar cuándo puede volver a usar el búfer. Esto evita que un filtro sobrescriba un búfer que sigue usando otro filtro. Un ejemplo no vuelve al grupo del asignador de muestras disponibles hasta que todos los filtros lo han liberado.

Para obtener más información, vea los temas siguientes:

-   En el tema [ejemplos y asignadores](samples-and-allocators.md) se proporciona una descripción más detallada de cómo funcionan los asignadores.
-   El [flujo de datos del tema en el gráfico de filtros](data-flow-in-the-filter-graph.md) proporciona una introducción general del flujo de datos en DirectShow.

Los temas siguientes están destinados a los desarrolladores que escriben sus propios filtros personalizados:

-   [Flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md)
-   [Subprocesos y secciones críticas](threads-and-critical-sections.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El gráfico de filtro y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



