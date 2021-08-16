---
title: Montones compartidos
description: El uso compartido es útil para arquitecturas de varios procesos y adaptadores.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e1bc0826651334d3d137466cc34d194fb79ae4900075b9a145859c5fd37fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300816"
---
# <a name="shared-heaps"></a>Montones compartidos

El uso compartido es útil para arquitecturas de varios procesos y adaptadores.

-   [Introducción al uso compartido](#sharing-overview)
-   [Uso compartido de montones entre procesos](#sharing-heaps-across-processes)
-   [Uso compartido de montones entre adaptadores](#sharing-heaps-across-adapters)
-   [Temas relacionados](#related-topics)

## <a name="sharing-overview"></a>Introducción al uso compartido

Los montones compartidos permiten dos cosas: compartir datos en un montón entre uno o varios procesos y, además, se excluye una opción no determinista de diseño de textura indefinido para los recursos colocados dentro del montón. El uso compartido de montones entre adaptadores también elimina la necesidad de serializar la CPU de los datos.

Se pueden compartir los montones y los recursos confirmados. Compartir un recurso confirmado comparte realmente el montón implícito junto con la descripción del recurso confirmado, de forma que se pueda asignar una descripción de recurso compatible al montón desde otro dispositivo.

Todos los métodos son de subproceso libre y heredan la semántica D3D11 existente del diseño de uso compartido del identificador NT.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Uso compartido de montones entre procesos

Los montones compartidos se especifican con el miembro D3D12 HEAP FLAG SHARED de la \_ \_ \_ [**enumeración D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Los montones compartidos no se admiten en montones accesibles para CPU: D3D12 \_ HEAP \_ TYPE \_ UPLOAD, D3D12 \_ HEAP TYPE READBACK y \_ \_ D3D12 \_ HEAP TYPE CUSTOM sin \_ \_ D3D12 \_ CPU PAGE PROPERTY NOT \_ \_ \_ \_ AVAILABLE.

Si se excluye una opción no determinista de diseño de textura indefinido, puede afectar significativamente a los escenarios de representación diferida en algunas GPU, por lo que no es el comportamiento predeterminado para los recursos colocados y confirmados. La representación diferida se ve afectada en algunas arquitecturas de GPU porque los diseños de textura deterministas reducen el ancho de banda de memoria efectivo que se logra al representar simultáneamente en varias texturas de destino de representación del mismo formato y tamaño. Las arquitecturas de GPU están evolucionando lejos de aprovechar los diseños de textura no deterministas para admitir patrones de swzzle estandarizados y diseños estandarizados de forma eficaz para la representación diferida.

Los montones compartidos también incluyen otros costos menores:

-   Los datos del montón compartido no se pueden reciclar de forma tan flexible como los montones en proceso debido a problemas de divulgación de información, por lo que la memoria física no se recicla con más frecuencia.
-   Hay una pequeña sobrecarga adicional de CPU y un aumento del uso de memoria del sistema durante la creación y destrucción de montones compartidos.

## <a name="sharing-heaps-across-adapters"></a>Uso compartido de montones entre adaptadores

Los montones compartidos entre adaptadores se especifican con el miembro D3D12 HEAP FLAG SHARED CROSS ADAPTER de la enumeración \_ \_ \_ \_ \_ [**D3D12 \_ HEAP \_ FLAGS.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)

Los montones compartidos entre adaptadores permiten que varios adaptadores compartan datos sin que la CPU serializa los datos entre ellos. Aunque las distintas funcionalidades del adaptador determinan cómo los adaptadores eficaces pueden pasar datos entre ellos, la simple habilitación de copias de GPU aumenta el ancho de banda efectivo logrado. Algunos diseños de textura se permiten en montones de adaptadores cruzados para admitir un intercambio de datos de textura, incluso si estos diseños de textura no se admiten de otro modo. Se pueden aplicar ciertas restricciones a dichas texturas, como admitir solo la copia.

El uso compartido entre adaptadores funciona con montones creados mediante una llamada [**a ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). A continuación, las aplicaciones pueden crear [**recursos a través de CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource). También lo permiten los recursos o montones creados por [**CreateCommittedResource,**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) pero solo para los recursos TEXTURE2D de dimensión de recursos D3D12 principales de fila (consulte DIMENSIÓN DE RECURSOS \_ \_ \_ [**D3D12 \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). El uso compartido entre adaptadores no funciona [**con CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

Para el uso compartido entre adaptadores, se siguen aplicando todas las reglas habituales de uso compartido de recursos entre colas. Las aplicaciones deben emitir las barreras adecuadas para garantizar la correcta sincronización y coherencia entre los dos adaptadores. Las aplicaciones deben usar barreras entre adaptadores para coordinar la programación de listas de comandos enviadas a varios adaptadores. No hay ningún mecanismo para compartir recursos entre adaptadores entre versiones de API D3D. Los recursos compartidos entre adaptadores solo se admiten en la memoria del sistema. Los montones o recursos compartidos entre adaptadores se admiten en los montones D3D12 HEAP TYPE DEFAULT y \_ \_ \_ D3D12 \_ HEAP \_ TYPE CUSTOM \_ (con el grupo de memoria L0 y las propiedades de página de CPU de combinación de escritura). Los controladores deben asegurarse de que las operaciones de lectura y escritura de GPU para montones compartidos entre adaptadores sean coherentes con otras GPU del sistema. Por ejemplo, es posible que el controlador tenga que excluir los datos del montón de residir en cachés de GPU que normalmente no necesitan vaciarse cuando la CPU no puede acceder directamente a los datos del montón.

Las aplicaciones deben limitar el uso de montones entre adaptadores solo a los escenarios que requieren la funcionalidad que proporcionan. Los montones entre adaptadores se encuentran en D3D12 MEMORY POOL L0, que no siempre es \_ \_ lo que sugiere \_ [**GetCustomHeapProperties.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) Ese grupo de memoria no es eficaz para las arquitecturas de adaptador NUMA o discretas. Además, los diseños de textura más eficaces no siempre están disponibles.

También se aplican las siguientes limitaciones:

-   Las marcas de montón relacionadas con los niveles del montón deben ser D3D12 \_ HEAP FLAG ALLOW ALL BUFFERS AND TEXTURES (PERMITIR TODOS LOS \_ \_ \_ \_ BÚFERES Y \_ \_ TEXTURAS).
-   También se debe establecer D3D12 \_ HEAP \_ FLAG \_ SHARED.
-   Debe establecerse D3D12 HEAP TYPE DEFAULT o \_ \_ \_ D3D12 \_ HEAP \_ TYPE CUSTOM con \_ D3D12 MEMORY POOL L0 y \_ \_ \_ D3D12 \_ CPU PAGE PROPERTY NOT \_ \_ \_ \_ AVAILABLE.
-   Solo los recursos con D3D12 RESOURCE FLAG ALLOW CROSS ADAPTER se pueden colocar en montones entre \_ \_ \_ \_ \_ adaptadores.

Para obtener más información sobre el uso de varios adaptadores, consulte la [sección Sistemas de varios adaptadores.](multi-engine.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subasignación en los búferes](suballocation-within-heaps.md)
</dt> </dl>

 

 




