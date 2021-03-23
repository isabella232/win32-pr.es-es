---
title: Alias de memoria y herencia de datos
description: Los recursos colocados y reservados pueden asignar un alias a la memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que los recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104505"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Alias de memoria y herencia de datos

Los recursos colocados y reservados pueden asignar un alias a la memoria física dentro de un montón. Los recursos colocados permiten más escenarios de herencia de datos que los recursos reservados cuando el montón tiene establecida la marca compartida o cuando los recursos con alias tienen diseños de memoria totalmente definidos.

-   [Establecimiento de alias](#memory-aliasing-and-data-inheritance)
-   [Herencia de datos](#data-inheritance)
-   [Temas relacionados](#related-topics)

## <a name="aliasing"></a>Establecimiento de alias

Se debe emitir una barrera de alias entre el uso de dos recursos que comparten la misma memoria física, incluso si no se desea la herencia de datos. Los modelos de uso simples deben indicar, como mínimo, el recurso de destino implicado en una operación de este tipo. Consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) para obtener más información y modelos de uso avanzado.

Una vez que se tiene acceso a un recurso, se invalidan todos los recursos que comparten la memoria física con ese recurso, a menos que se permita la herencia de datos. Las lecturas de recursos invalidados dan lugar a contenido de recursos sin definir. Las operaciones de escritura en recursos invalidados también producen contenido de recursos sin definir, a menos que se produzcan dos condiciones:

-   El recurso no tiene la \_ marca de recurso D3D12 \_ permitir \_ el \_ \_ destino de representación o el \_ marcador de recurso D3D12 permitir la marca de \_ \_ \_ profundidad \_ .
-   La escritura es una operación de copiar o borrar en un icono o un subrecurso completo. La inicialización en mosaico solo está disponible para los recursos con el icono de 64 KB \_ \_ \_ SWIZZLE y el estándar de mosaico de 64 KB \_ \_ \_ SWIZZLE.

Las invalidaciones superpuestas se limitan a granularidad más reducida, cuando los diseños proporcionan información sobre la ubicación de los datos de textura y cuando los recursos se encuentran en determinados Estados de barrera de transición. Sin embargo, las invalidaciones no pueden ir más pequeñas que las granularidades de la alineación de recursos.

Una granularidad de alineación del búfer es de 64 KB y la granularidad de alineación mayor tiene prioridad. Esto es importante al considerar las texturas de 4 KB, ya que pueden residir varias texturas de 4 KB en una región de 64 KB sin superponerse entre sí. Pero no se puede usar un alias de búfer de la misma región de 64 KB junto con ninguna de esas texturas de 4 KB. La aplicación no puede mantener de forma confiable el acceso al búfer desde la intersección de las texturas de 4 KB, ya que las GPU pueden swizzle datos de textura de 4 KB dentro de la región de 64 KB en un patrón no definido.

\_los diseños de mosaico no definidos de 64 KB \_ \_ SWIZZLE, estándar de iconos de 64 KB \_ y de \_ \_ textura principal de fila \_ informan a la aplicación de qué granularidad de alineación superpuestas han dejado de ser válidas. Por ejemplo: una aplicación puede crear una matriz de textura de destino de representación 2D con dos segmentos de matriz, un solo nivel de MIP y el \_ \_ diseño de SWIZZLE sin definir de mosaico de 64 KB \_ . Supongamos que la aplicación entiende que cada segmento de la matriz ocupa 100 iconos de 64 KB. La aplicación puede renunciar al uso del segmento 0 de la matriz y volver a usar esa memoria para un búfer de ~ 6 MB, una textura de ~ 6 MB con diseño sin definir, etc. Más adelante, supongamos que la aplicación ya no necesita el primer mosaico del segmento 1 de la matriz. A continuación, la aplicación también podría encontrar un búfer de 64 KB allí hasta que la representación requiera el primer mosaico del segmento 1 de la matriz. La aplicación tendría que hacer un borrado o una copia de icono completo para volver a usar el primer icono con la matriz de texturas de nuevo.

Sin embargo, incluso las texturas con diseños definidos todavía tienen casos problemáticos. Los tamaños de los recursos de textura pueden diferir significativamente de lo que la aplicación puede calcular, ya que algunas arquitecturas de adaptador asignan memoria adicional para las texturas con el fin de reducir el ancho de banda efectivo durante escenarios de representación comunes. Cualquier invalidación en esa región de memoria adicional hará que se invalide todo el recurso. Consulte [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) para obtener más información.

## <a name="data-inheritance"></a>Herencia de datos

Los recursos colocados permiten la mayor herencia de datos para las texturas, incluso con diseños de memoria no definidos. Las aplicaciones pueden imitar las capacidades de herencia de datos que los recursos compartidos comprometieron habilitar buscando dos texturas con propiedades de recursos idénticas en el mismo desplazamiento en un montón compartido. La descripción completa del recurso debe ser idéntica, incluido el valor sin cifrar optimizado y el tipo de método de creación de recursos (colocada o reservada). Sin embargo, ambos recursos pueden tener Estados de barrera de transición inicial diferentes.

Los recursos reservados permiten la herencia de datos por mosaico; pero las restricciones existen normalmente para los Estados de barrera de transición de recursos.

Para heredar los datos, ambos recursos deben estar en un estado de barrera de transición de recursos compatible:

-   En el caso de los búferes, las texturas de acceso simultáneo y las texturas entre adaptadores, el estado de la transición de recursos no es importante y todos los Estados son "compatibles".
-   En el caso de las texturas reservadas sin las propiedades anteriores u otra herencia de datos por icono a través del icono de 64 KB \_ \_ \_ SWIZZLE o el estándar de mosaico de 64 KB \_ \_ \_ SWIZZLE, el estado de la barrera de transición de recursos que incluye el icono debe estar en el Estado común.
-   Para todas las demás texturas, donde las descripciones de recursos coinciden exactamente, el estado de la barrera de transición de recursos para cada par de Subrecursos correspondiente debe:
    -   Estar en el Estado común.
    -   Ser igual cuando el estado tiene la misma marca GPU-escritura.

Cuando la GPU admite swizzle estándar, los búferes y las texturas de swizzle estándar pueden tener un alias para la misma memoria y heredar los datos entre ellos. La aplicación puede manipular textura desde la representación del búfer, porque el patrón swizzle estándar describe cómo se colocan los textura en la memoria. El patrón swizzle de CPU-visible es equivalente al patrón de swizzle visible para GPU que se ve en los búferes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación dentro de montones](suballocation-within-heaps.md)
</dt> </dl>

 

 




