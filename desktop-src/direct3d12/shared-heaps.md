---
title: Montones compartidos
description: Compartir es útil para arquitecturas multiproceso y multiadaptador.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/26/2019
ms.locfileid: "74103839"
---
# <a name="shared-heaps"></a>Montones compartidos

Compartir es útil para arquitecturas multiproceso y multiadaptador.

-   [Información general de uso compartido](#sharing-overview)
-   [Uso compartido de montones entre procesos](#sharing-heaps-across-processes)
-   [Uso compartido de montones entre adaptadores](#sharing-heaps-across-adapters)
-   [Temas relacionados](#related-topics)

## <a name="sharing-overview"></a>Información general de uso compartido

Los montones compartidos permiten dos cosas: compartir datos en un montón en uno o varios procesos y evitar una elección no determinista del diseño de textura sin definir para los recursos que se colocan en el montón. El uso compartido de montones entre adaptadores también elimina la necesidad de calcular las referencias de la CPU de los datos.

Se pueden compartir tanto montones como recursos confirmados. Compartir un recurso confirmado realmente comparte el montón implícito junto con la descripción del recurso confirmado, de modo que se puede asignar una descripción del recurso compatible al montón desde otro dispositivo.

Todos los métodos son de subprocesamiento libre y heredan la semántica D3D11 existente del diseño de uso compartido de identificadores NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Uso compartido de montones entre procesos

Los montones compartidos se especifican con el \_ \_ \_ miembro compartido de la marca de montón D3D12 de la enumeración [**D3D12 \_ heap \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

No se admiten montones compartidos en montones accesibles desde la CPU: D3D12 de tipo \_ \_ de montón \_ D3D12, \_ tipo de montón \_ \_ READBACK y D3D12 \_ tipo de montón \_ \_ personalizado sin la propiedad de \_ Página CPU de D3D12 \_ \_ \_ no \_ disponible.

Impedir una elección no determinista del diseño de textura sin definir puede perjudicar significativamente escenarios de representación aplazados en algunas GPU, por lo que no es el comportamiento predeterminado de los recursos colocados y confirmados. La representación diferida está desemparejada en algunas arquitecturas de GPU porque los diseños de texturas deterministas reducen el ancho de banda de memoria efectivo que se logra al representar simultáneamente en varias texturas de destino de representación con el mismo formato y tamaño. Las arquitecturas de GPU no aprovechan los diseños de texturas no deterministas con el fin de admitir patrones normalizados de swizzle y diseños estandarizados de forma eficaz para la representación diferida.

Los montones compartidos también tienen otros costos menores:

-   Los datos del montón compartido no se pueden reciclar como montones en proceso debido a problemas de divulgación de información, por lo que la memoria física se zero'ed con más frecuencia.
-   Hay una sobrecarga de CPU adicional y un mayor uso de la memoria del sistema durante la creación y destrucción de montones compartidos.

## <a name="sharing-heaps-across-adapters"></a>Uso compartido de montones entre adaptadores

Los montones compartidos entre adaptadores se especifican con \_ la \_ marca \_ de montón D3D12 \_ miembro compartido Cross \_ Adapter de la enumeración [**D3D12 \_ heap \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) .

Los montones compartidos de adaptador cruzado permiten que varios adaptadores compartan datos sin calcular las referencias de la CPU de los datos entre ellos. Mientras que las distintas funcionalidades de adaptador determinan cómo los adaptadores eficientes pueden pasar datos entre ellos, la simple habilitación de las copias de GPU aumenta el ancho de banda efectivo conseguido. Algunos diseños de textura están permitidos en montones de adaptadores cruzados para admitir un intercambio de datos de textura, incluso si no se admiten estos diseños de textura. Se pueden aplicar determinadas restricciones a estas texturas, como solo admitir la copia.

El uso compartido entre adaptadores funciona con montones creados mediante una llamada a [**ID3D12Device:: CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Las aplicaciones pueden crear recursos a través de [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). También lo permiten los recursos o montones creados por [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) , pero solo para los recursos de D3D12 de \_ dimensión de recursos TEXTURE2D principales de fila \_ \_ (consulte la [**dimensión de \_ recursos \_ de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). El uso compartido entre adaptadores no funciona con [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

Para el uso compartido entre adaptadores, se siguen aplicando todas las reglas habituales de uso compartido de recursos entre colas. Las aplicaciones deben emitir las barreras adecuadas para garantizar la sincronización correcta y la coherencia entre los dos adaptadores. Las aplicaciones deben usar barreras entre adaptadores para coordinar la programación de las listas de comandos enviadas a varios adaptadores. No hay ningún mecanismo para compartir recursos entre adaptadores a través de las versiones de la API de D3D. Los recursos compartidos entre adaptadores solo se admiten en la memoria del sistema. Los recursos o montones compartidos entre adaptadores se admiten en montones \_ \_ predeterminados de tipo de montón D3D12 y en \_ \_ montones personalizados de tipo de montón D3D12 \_ \_ (con el grupo de memoria L0 y las propiedades de la página CPU de lectura y combinación). Los controladores deben asegurarse de que las operaciones de lectura y escritura de GPU en montones compartidos entre adaptadores son coherentes con otras GPU del sistema. Por ejemplo, es posible que el controlador tenga que excluir los datos del montón de residir en memorias caché de GPU que normalmente no es necesario vaciar cuando la CPU no puede acceder directamente a los datos del montón.

Las aplicaciones deben limitar el uso de montones de adaptadores cruzados solo a los escenarios que requieren la funcionalidad que proporcionan. Los montones de adaptadores cruzados se encuentran en \_ el grupo de memoria D3D12 \_ \_ L0, que no siempre es lo que [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) sugiere. El bloque de memoria no es eficaz para las arquitecturas de adaptador discreto/NUMA. Además, los diseños de textura más eficientes no están siempre disponibles.

También se aplican las siguientes limitaciones:

-   Las marcas del montón relacionadas con los niveles del montón deben ser D3D12 el \_ indicador de montón \_ \_ permiten \_ todos los \_ búferes \_ y \_ texturas.
-   \_ \_ También se debe establecer la marca de montón D3D12 \_ compartida.
-   Debe establecerse el tipo predeterminado de montón de D3D12 \_ \_ o el \_ \_ \_ tipo de montón D3D12 \_ personalizado con el \_ grupo de memoria D3D12 \_ \_ L0 y la \_ propiedad de página de CPU D3D12 \_ \_ \_ no \_ disponible.
-   Solo los recursos con la \_ marca de recurso D3D12 permiten el \_ \_ \_ \_ adaptador cruzado en montones entre adaptadores.

Para obtener más información sobre el uso de varios adaptadores, consulte la sección [sistemas de varios adaptadores](multi-engine.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación dentro de montones](suballocation-within-heaps.md)
</dt> </dl>

 

 




