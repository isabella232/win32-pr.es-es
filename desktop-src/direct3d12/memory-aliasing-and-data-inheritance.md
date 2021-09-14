---
title: Alias de memoria y herencia de datos
description: Los recursos colocados y reservados pueden crear un alias de memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072946"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Alias de memoria y herencia de datos

Los recursos colocados y reservados pueden crear un alias de memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos.

-   [Establecimiento de alias](#memory-aliasing-and-data-inheritance)
-   [Herencia de datos](#data-inheritance)
-   [Temas relacionados](#related-topics)

## <a name="aliasing"></a>Establecimiento de alias

Se debe emitir una barrera de alias entre el uso de dos recursos que comparten la misma memoria física, incluso si no se desea la herencia de datos. Los modelos de uso simples deben indicar, al menos, el recurso de destino implicado en esta operación. Consulte [**CreatePlacedResource para**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) obtener más detalles y modelos de uso avanzados.

Una vez que se accede a un recurso, todos los recursos que comparten memoria física con ese recurso se invalidan, a menos que se permita la herencia de datos. Las lecturas de recursos invalidados tienen como resultado contenido de recursos indefinidos. Las escrituras en recursos invalidados también dan lugar a contenidos de recursos indefinidos, a menos que se produzcan dos condiciones:

-   El recurso no tiene la MARCA DE RECURSOS D3D12 ALLOW RENDER TARGET o la MARCA DE RECURSOS \_ \_ \_ \_ \_ D3D12 \_ \_ ALLOW DEPTH \_ \_ \_ STENCIL.
-   La escritura es una operación de copia o despejado en un subrecurso o icono completo. La inicialización de mosaicos solo está disponible para los recursos con 64 KB \_ TILE \_ UNDEFINED \_ SWZZLE y 64 KB \_ TILE STANDARD \_ \_ SWZZLE.

Las invalidaciones superpuestas se limita a granularidades más pequeñas, cuando los diseños proporcionan información sobre la ubicación de los datos de textura y cuándo los recursos se encuentran en determinados estados de barrera de transición. Sin embargo, las invalidaciones no pueden ser más pequeñas que las granularidades de alineación de recursos.

Una granularidad de alineación de búfer es de 64 KB y la granularidad de alineación mayor tiene prioridad. Esto es importante al considerar las texturas de 4 KB, ya que varias texturas de 4 KB pueden residir en una región de 64 KB sin superponerse entre sí. Pero no se puede usar un alias de búfer que tenga la misma región de 64 KB junto con ninguna de esas texturas de 4 KB. La aplicación no puede evitar de forma confiable que el acceso al búfer se intersece con las texturas de 4 KB, ya que las GPU pueden deslizar datos de textura de 4 KB dentro de la región de 64 KB en un patrón indefinido.

Los diseños de textura \_ \_ TILE \_ UNDEFINED SW GRANULARLE, 64KB TILE STANDARD SW GRANULARLE y ROW MAJOR de 64 KB informan a la aplicación de que las granularidades de alineación superpuestas han pasado a ser \_ no \_ \_ \_ válidas. Por ejemplo: una aplicación puede crear una matriz de textura de destino de representación 2D con 2 segmentos de matriz, un único nivel de mip y el diseño \_ \_ SWZZLE UNDEFINED TILE de 64 \_ KB. Supongamos que la aplicación entiende que cada segmento de matriz ocupa iconos de 100 64 KB. La aplicación puede usar el segmento de matriz 0 y volver a usar esa memoria para un búfer de ~6 MB, una textura de ~6 MB con un diseño indefinido, etc. Más adelante, suponga que la aplicación ya no requiere el primer icono del segmento 1 de la matriz. A continuación, la aplicación también podría encontrar un búfer de 64 KB allí hasta que la representación requeriría de nuevo el primer icono del segmento 1 de la matriz. La aplicación tendría que borrar o copiar un icono completo para volver a usar el primer icono con la matriz de texturas de nuevo.

Sin embargo, incluso las texturas con diseños definidos siguen teniendo casos problemáticos. Los tamaños de los recursos de textura pueden diferir significativamente de lo que la aplicación puede calcular a sí misma, ya que algunas arquitecturas de adaptador asignan memoria adicional para las texturas a fin de reducir el ancho de banda efectivo durante los escenarios de representación comunes. Las invalidaciones en esa región de memoria adicional hacen que todo el recurso se invalide. Consulte [**GetResourceAllocationInfo para**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) obtener más detalles.

## <a name="data-inheritance"></a>Herencia de datos

Los recursos colocados permiten la mayoría de la herencia de datos para texturas, incluso con diseños de memoria indefinidos. Las aplicaciones pueden imitar las funcionalidades de herencia de datos que habilitan los recursos confirmados compartidos mediante la localización de dos texturas con propiedades de recursos idénticas en el mismo desplazamiento en un montón compartido. La descripción completa del recurso debe ser idéntica, incluido el valor sin formato optimizado y el tipo de método de creación de recursos (colocado o reservado). Sin embargo, es posible que ambos recursos tengan estados de barrera de transición iniciales diferentes.

Los recursos reservados permiten la herencia de datos por icono; pero normalmente existen restricciones para los estados de barrera de transición de recursos.

Para heredar datos, ambos recursos deben estar en un estado de barrera de transición de recursos compatible:

-   Para los búferes, las texturas de acceso simultáneas y las texturas entre adaptadores, el estado de transición de recursos no es importante y todos los estados son "compatibles".
-   En el caso de las texturas reservadas sin las propiedades anteriores u otra herencia de datos por mosaico a través de 64 KB \_ TILE \_ \_ UNDEFINED SWZZLE o 64 KB \_ TILE STANDARD \_ \_ SWZZLE, el estado de barrera de transición de recursos, incluido el icono, debe estar en el estado común.
-   Para todas las demás texturas, donde las descripciones de recursos coinciden exactamente, el estado de la barrera de transición de recursos para cada par correspondiente de subrecursos debe:
    -   Estar en el estado común.
    -   Ser igual cuando el estado tenga la misma marca de escritura por GPU.

Cuando la GPU admite swzzle estándar, los búferes y las texturas de swzzle estándar se pueden usar como alias en la misma memoria y heredar los datos entre ellos. La aplicación puede manipular los elementos de textura de la representación del búfer, ya que el patrón swzzle estándar describe cómo se scriben los elementos de textura en la memoria. El patrón swzzle visible para LA CPU es equivalente al patrón swzzle visible para GPU que se ve en los búferes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación en los búferes](suballocation-within-heaps.md)
</dt> </dl>

 

 




