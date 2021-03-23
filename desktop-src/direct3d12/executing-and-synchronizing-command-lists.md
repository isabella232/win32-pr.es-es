---
title: Ejecutar y sincronizar listas de comandos
description: En Microsoft Direct3D 12, el modo inmediato de versiones anteriores ya no está presente.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- lista de comandos
- sincronización
- ejecución
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef910463ba3a771ac142d41309ae590884e3bc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549188"
---
# <a name="executing-and-synchronizing-command-lists"></a>Ejecutar y sincronizar listas de comandos

En Microsoft Direct3D 12, el modo inmediato de versiones anteriores ya no está presente. En su lugar, las aplicaciones crean listas y agrupaciones de comandos y, a continuación, registran conjuntos de comandos de GPU. Las colas de comandos se usan para enviar listas de comandos que se van a ejecutar. Este modelo permite a los desarrolladores tener más control sobre el uso eficaz de la unidad de procesamiento de gráficos (GPU) y la CPU.

-   [Información general sobre la cola de comandos](#command-queue-overview)
-   [Inicializar una cola de comandos](#initializing-a-command-queue)
-   [Ejecutar listas de comandos](#executing-command-lists)
-   [Acceso a recursos desde varias colas de comandos](#accessing-resources-from-multiple-command-queues)
-   [Sincronizar la ejecución de la lista de comandos mediante vallas de cola de comandos](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Sincronizar recursos a los que tienen acceso las colas de comandos](#synchronizing-resources-accessed-by-command-queues)
-   [Compatibilidad de cola de comandos para recursos en mosaico](#command-queue-support-for-tiled-resources)
-   [Temas relacionados](#related-topics)

## <a name="command-queue-overview"></a>Información general sobre la cola de comandos

Las colas de comandos de Direct3D 12 reemplazan el tiempo de ejecución y la sincronización de controladores del envío de trabajo de modo inmediato, que anteriormente no se expuso al desarrollador, con las API para administrar explícitamente la simultaneidad, el paralelismo y la sincronización. Las colas de comandos proporcionan las siguientes mejoras para los desarrolladores:

-   Permite a los desarrolladores evitar ineficiencias accidentales causados por una sincronización inesperada.
-   Permite a los desarrolladores introducir la sincronización en un nivel superior en el que la sincronización necesaria se puede determinar de forma más eficaz y precisa. Esto significa que el tiempo de ejecución y el controlador de gráficos gastarán menos tiempo reactivamente el paralelismo de ingeniería.
-   Hace que las operaciones costosas sean más explícitas.

Estas mejoras habilitan o mejoran los siguientes escenarios:

-   Mayor paralelismo: las aplicaciones pueden usar colas más profundas para cargas de trabajo en segundo plano, como la descodificación de vídeo, cuando tienen colas independientes para el trabajo en primer plano.
-   Trabajo de GPU asincrónica y de prioridad baja: el modelo de cola de comandos permite la ejecución simultánea de trabajo de GPU de baja prioridad y operaciones atómicas que permiten que un subproceso de GPU consuma los resultados de otro subproceso no sincronizado sin bloqueos.
-   Trabajo de proceso de alta prioridad: este diseño permite escenarios en los que es necesario interrumpir la representación en 3D para realizar una pequeña cantidad de trabajo de proceso de alta prioridad, de modo que el resultado pueda obtenerse pronto para el procesamiento adicional en la CPU.

## <a name="initializing-a-command-queue"></a>Inicializar una cola de comandos

Las colas de comandos se pueden crear mediante una llamada a [**ID3D12Device:: CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue). Este método toma un [**\_ tipo de \_ lista \_ de comandos D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) que indica el tipo de cola que se debe crear y, por tanto, el tipo de comandos que se puede enviar a esa cola. Recuerde que los paquetes solo se pueden llamar desde listas de comandos directas y no se pueden enviar directamente a una cola. Los tipos de cola admitidos son:

-   [**Tipo de lista de comandos de D3D12 \_ \_ \_ \_ directo**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Tipo de lista de comandos D3D12 \_ \_ \_ Compute**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Copia de \_ tipo de lista de comandos de D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

En general, las colas directas y las listas de comandos aceptan cualquier comando, las colas de proceso y las listas de comandos aceptan comandos relacionados con el cálculo y la copia, y las listas de comandos copiar y colas solo aceptan comandos de copia.

## <a name="executing-command-lists"></a>Ejecutar listas de comandos

Después de haber registrado una lista de comandos y de recuperar la cola de comandos predeterminada o de crear una nueva, se ejecutan las listas de comandos mediante una llamada a [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Las aplicaciones pueden enviar listas de comandos a cualquier cola de comandos desde varios subprocesos. El tiempo de ejecución realizará el trabajo de serialización de estas solicitudes en el orden de envío.

El Runtime validará la lista de comandos enviada y quitará la llamada a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) si se infringe alguna de las restricciones. Las llamadas se quitarán por los siguientes motivos:

-   La lista de comandos proporcionada es un paquete, no una lista de comandos directa.
-   No se ha llamado a [**ID3D12GraphicsCommandList:: Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) en la lista de comandos proporcionada para completar la grabación.
-   Se ha llamado a [**ID3D12CommandAllocator:: RESET**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) en el asignador de comandos asociado a la lista de comandos desde que se grabó. Para obtener más información acerca de los asignadores de comandos, vea [crear y grabar listas de comandos y agrupaciones](recording-command-lists-and-bundles.md).
-   La barrera de la cola de comandos indica que aún no se ha completado una ejecución anterior de la lista de comandos. Las barreras de la cola de comandos se describen con más detalle a continuación.
-   Los Estados antes y después de las consultas, establecido con llamadas a [**ID3D12GraphicsCommandList:: BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**ID3D12GraphicsCommandList:: EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), no coinciden correctamente.
-   Los Estados antes y después de las barreras de la transición de recursos no coinciden correctamente. Para obtener más información, consulte [uso de barreras de recursos para sincronizar los Estados de los recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="accessing-resources-from-multiple-command-queues"></a>Acceso a recursos desde varias colas de comandos

Hay un par de reglas impuestas por el motor en tiempo de ejecución que restringen el acceso a los recursos desde varias colas de comandos. Estas reglas son:

<dl> 1. No se puede escribir un recurso en desde varias colas de comandos simultáneamente. Cuando un recurso ha pasado a un estado grabable en una cola, se considera que es propiedad exclusiva de esa cola y debe realizar la transición a un estado de lectura o común (consulte <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">**\_ \_ los Estados de los recursos de D3D12**</a>) antes de que otra cola pueda acceder a él.  </dl>
<dl> 2. Cuando se está en un estado de lectura, se puede leer un recurso desde varias colas de comandos simultáneamente, incluidos los procesos, en función de su estado de lectura. </dl>

Para obtener más información sobre las restricciones de acceso a recursos y el uso de barreras de recursos para sincronizar el acceso a los recursos, consulte [uso de barreras de recursos para sincronizar los Estados de los recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Sincronizar la ejecución de la lista de comandos mediante vallas de cola de comandos

La compatibilidad con varias colas de comandos paralelas en Direct3D 12 ofrece más flexibilidad y control sobre la priorización del trabajo asincrónico en la GPU. Este diseño también significa que las aplicaciones deben administrar explícitamente la sincronización del trabajo, especialmente cuando las listas de comandos en una cola dependen de los recursos en los que se está trabajando en otra cola de comandos. Algunos ejemplos de esto incluyen la espera de que una operación en una cola de proceso se complete, de modo que el resultado pueda usarse para una operación de representación en la cola 3D y esperar a que se complete una operación 3D para que una operación en la cola de proceso pueda tener acceso a un recurso para su escritura. Para habilitar la sincronización del trabajo entre las colas, Direct3D 12 usa el concepto de vallas, que se representan en la API mediante la interfaz [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) .

Una barrera es un entero que representa la unidad de trabajo actual que se está procesando. Cuando la aplicación avanza la barrera, al llamar a [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal), se actualiza el entero. Las aplicaciones pueden comprobar el valor de una barrera y determinar si se ha completado una unidad de trabajo con el fin de decidir si se puede iniciar una operación posterior.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Sincronizar recursos a los que tienen acceso las colas de comandos

En Direct3D 12, la sincronización del estado de algunos recursos se implementa con barreras de recursos. En cada barrera de recursos, una aplicación declara los Estados antes y después de un recurso. Un ejemplo común es que un recurso cambie entre una vista de recursos del sombreador a una vista de destino de representación. En su mayor parte, estas barreras de recursos se administran dentro de las listas de comandos. Cuando se habilitan las capas de depuración, el sistema exige que los Estados antes y después de todos los recursos coincidan, lo que garantiza que el recurso se encuentre en el estado correcto para una operación determinada en una transición de barrera.

Para obtener más información sobre cómo sincronizar el estado de los recursos, consulte [uso de barreras de recursos para sincronizar los Estados de los recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="command-queue-support-for-tiled-resources"></a>Compatibilidad de cola de comandos para recursos en mosaico

Los métodos para administrar los recursos en mosaico, que se exponían a través de la interfaz [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) en Direct3D 11, se proporcionan mediante la interfaz [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) en Direct3D 12. Esos métodos incluyen:



| Método                                                              | Descripción                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copia las asignaciones de un recurso de origen en mosaico a un recurso en mosaico de destino.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Actualiza las asignaciones de ubicaciones de iconos en recursos en mosaico a ubicaciones de memoria en un montón de recursos.<br/> |



 

Para obtener más información sobre el uso de recursos en mosaico en aplicaciones de Direct3D 12, consulte [Direct3D 11 de los recursos en mosaico](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Envío de trabajo en Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

