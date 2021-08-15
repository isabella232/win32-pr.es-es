---
title: Ejecución y sincronización de listas de comandos
description: En Microsoft Direct3D 12, el modo inmediato de las versiones anteriores ya no está presente.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- lista de comandos
- sincronización
- ejecución
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41677ee1bc17fb2a935f157d969352617c0d5c3c15eb38a76225b3a8c71e7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529145"
---
# <a name="executing-and-synchronizing-command-lists"></a>Ejecución y sincronización de listas de comandos

En Microsoft Direct3D 12, el modo inmediato de las versiones anteriores ya no está presente. En su lugar, las aplicaciones crean listas de comandos y agrupan y, a continuación, registran conjuntos de comandos de GPU. Las colas de comandos se usan para enviar listas de comandos que se van a ejecutar. Este modelo permite a los desarrolladores tener más control sobre el uso eficaz de la unidad de procesamiento gráfico (GPU) y la CPU.

-   [Introducción a la cola de comandos](#command-queue-overview)
-   [Inicialización de una cola de comandos](#initializing-a-command-queue)
-   [Ejecutar listas de comandos](#executing-command-lists)
-   [Acceso a recursos desde varias colas de comandos](#accessing-resources-from-multiple-command-queues)
-   [Sincronización de la ejecución de la lista de comandos mediante barreras de cola de comandos](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Sincronización de recursos a los que acceden las colas de comandos](#synchronizing-resources-accessed-by-command-queues)
-   [Compatibilidad de la cola de comandos con recursos en mosaico](#command-queue-support-for-tiled-resources)
-   [Temas relacionados](#related-topics)

## <a name="command-queue-overview"></a>Introducción a la cola de comandos

Las colas de comandos de Direct3D 12 reemplazan el tiempo de ejecución y la sincronización del controlador del envío de trabajo en modo inmediato, que antes no se exponía al desarrollador, por API para administrar explícitamente la simultaneidad, el paralelismo y la sincronización. Las colas de comandos proporcionan las siguientes mejoras para los desarrolladores:

-   Permite a los desarrolladores evitar ineficiencias accidentales causadas por una sincronización inesperada.
-   Permite a los desarrolladores introducir la sincronización en un nivel superior donde la sincronización necesaria se puede determinar de forma más eficaz y precisa. Esto significa que el tiempo de ejecución y el controlador de gráficos dedicarán menos tiempo a la ingeniería de paralelismo.
-   Hace que las operaciones costosas sea más explícita.

Estas mejoras permiten o mejoran los escenarios siguientes:

-   Mayor paralelismo: las aplicaciones pueden usar colas más profundas para cargas de trabajo en segundo plano, como la decodificación de vídeo, cuando tienen colas independientes para el trabajo en primer plano.
-   Trabajo de GPU asincrónico y de prioridad baja: el modelo de cola de comandos permite la ejecución simultánea de operaciones atómicas y de trabajo de GPU de prioridad baja que permiten que un subproceso de GPU consuma los resultados de otro subproceso sin sincronizar sin bloquear.
-   Trabajo de proceso de alta prioridad: este diseño permite que los escenarios que requieren interrumpir la representación en 3D realicen una pequeña cantidad de trabajo de proceso de alta prioridad para que el resultado se pueda obtener pronto para un procesamiento adicional en la CPU.

## <a name="initializing-a-command-queue"></a>Inicialización de una cola de comandos

Las colas de comandos se pueden crear llamando a [**ID3D12Device::CreateCommandQueue.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) Este método toma un [**D3D12 \_ COMMAND \_ LIST \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) que indica qué tipo de cola se debe crear y, por lo tanto, qué tipo de comandos se pueden enviar a esa cola. Recuerde que las agrupaciones solo se pueden llamar desde listas de comandos directos y no se pueden enviar directamente a una cola. Los tipos de cola admitidos son:

-   [**D3D12 \_ COMMAND \_ LIST \_ TYPE \_ DIRECT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**PROCESO DE TIPO DE LISTA \_ DE COMANDOS D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ COMMAND \_ LIST \_ TYPE \_ COPY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

En general, las colas y listas de comandos de DIRECT aceptan cualquier comando, las colas COMPUTE y las listas de comandos aceptan comandos relacionados con el proceso y la copia, y las colas COPY y las listas de comandos solo aceptan comandos de copia.

## <a name="executing-command-lists"></a>Ejecutar listas de comandos

Después de registrar una lista de comandos y recuperar la cola de comandos predeterminada o de crear una nueva, ejecute listas de comandos llamando a [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Las aplicaciones pueden enviar listas de comandos a cualquier cola de comandos desde varios subprocesos. El tiempo de ejecución realizará el trabajo de serializar estas solicitudes en el orden de envío.

El tiempo de ejecución validará la lista de comandos enviados y quitará la llamada a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) si se infringe alguna de las restricciones. Las llamadas se descartarán por los siguientes motivos:

-   La lista de comandos proporcionada es una agrupación, no una lista de comandos directos.
-   [**No se ha llamado a ID3D12GraphicsCommandList::Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) en la lista de comandos proporcionada para completar la grabación.
-   Se ha llamado a [**ID3D12CommandAllocator::Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) en el asignador de comandos asociado a la lista de comandos desde que se registró. Para obtener más información sobre los asignadores de comandos, vea Creación y grabación de listas [de comandos y agrupaciones.](recording-command-lists-and-bundles.md)
-   La barrera de la cola de comandos indica que aún no se ha completado una ejecución anterior de la lista de comandos. Las barreras de cola de comandos se de abordan con detalle a continuación.
-   Los estados antes y después de las consultas, establecidos con llamadas a [**ID3D12GraphicsCommandList::BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**ID3D12GraphicsCommandList::EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), no coinciden correctamente.
-   Los estados antes y después de las barreras de transición de recursos no coinciden correctamente. Para más información, consulte [Uso de barreras de recursos para sincronizar estados de recursos.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="accessing-resources-from-multiple-command-queues"></a>Acceso a recursos desde varias colas de comandos

Hay un par de reglas impuestas por el tiempo de ejecución que restringen el acceso de recursos desde varias colas de comandos. Estas reglas son:

1. No se puede escribir un recurso en desde varias colas de comandos simultáneamente. Cuando un recurso ha pasado a un estado que se puede escribir en una cola, se considera propiedad exclusiva de esa cola y debe realizar la transición a un estado de lectura o COMMON (consulte [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) para que otra cola pueda acceder a él.

2. Cuando se encuentra en un estado de lectura, se puede leer un recurso de varias colas de comandos simultáneamente, incluidos los procesos, en función de su estado de lectura.

Para obtener más información sobre las restricciones de acceso a los recursos y el uso de barreras de recursos para sincronizar el acceso a los recursos, consulte Uso de barreras de recursos [para sincronizar los estados de los recursos.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Sincronización de la ejecución de la lista de comandos mediante barreras de cola de comandos

La compatibilidad con varias colas de comandos paralelas en Direct3D 12 proporciona más flexibilidad y control sobre la priorización del trabajo asincrónico en la GPU. Este diseño también significa que las aplicaciones deben administrar explícitamente la sincronización del trabajo, especialmente cuando las listas de comandos de una cola dependen de los recursos que opera otra cola de comandos. Algunos ejemplos de esto incluyen esperar a que se complete una operación en una cola de proceso para que el resultado se pueda usar para una operación de representación en la cola 3D y esperar a que se complete una operación 3D para que una operación en la cola de proceso pueda acceder a un recurso para escritura. Para habilitar la sincronización del trabajo entre colas, Direct3D 12 usa el concepto de barreras, que se representan en la API mediante la [**interfaz ID3D12Fence.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)

Una barrera es un entero que representa la unidad de trabajo actual que se está procesando. Cuando la aplicación avanza la barrera, llamando a [**ID3D12CommandQueue::Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal), se actualiza el entero. Las aplicaciones pueden comprobar el valor de una barrera y determinar si se ha completado una unidad de trabajo para decidir si se puede iniciar una operación posterior.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Sincronización de recursos a los que acceden las colas de comandos

En Direct3D 12, la sincronización del estado de algunos recursos se implementa con barreras de recursos. En cada barrera de recursos, una aplicación declara los estados antes y después de un recurso. Un ejemplo común es la transición de un recurso entre una vista de recursos de sombreador y una vista de destino de representación. En su mayor parte, estas barreras de recursos se administran en listas de comandos. Cuando se habilitan las capas de depuración, el sistema exige que los estados antes y después de todos los recursos coincidan, lo que garantiza que el recurso se encuentra en el estado correcto para una operación determinada en una transición de barrera.

Para obtener más información sobre cómo sincronizar el estado de los recursos, consulte [Uso de barreras de recursos para sincronizar estados de recursos.](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

## <a name="command-queue-support-for-tiled-resources"></a>Compatibilidad de la cola de comandos con recursos en mosaico

La interfaz [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) de Direct3D 12 proporciona métodos para administrar recursos en mosaico, que se han expuesto a través de la interfaz [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) en Direct3D 11. Esos métodos incluyen:



| Método                                                              | Descripción                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copia las asignaciones de un recurso en mosaico de origen a un recurso en mosaico de destino.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Actualiza las asignaciones de ubicaciones de mosaico de los recursos en mosaico a las ubicaciones de memoria de un montón de recursos.<br/> |



 

Para obtener más información sobre el uso de recursos en mosaico en aplicaciones de Direct3D 12, consulte Recursos en mosaico de [Direct3D11.](/windows/desktop/direct3d11/tiled-resources)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

