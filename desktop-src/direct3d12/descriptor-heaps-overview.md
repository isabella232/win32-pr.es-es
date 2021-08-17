---
title: Información general sobre los montones de descriptores
description: Los montones de descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como vistas de recursos de sombreador (SRV), vistas de acceso desordenado (UAV), vistas de búfer constante (CBV) y muestreadores.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d0017f10a6027fc7ce48618a9d28bd4e92262d83d0f3aa81cc0bc8d02b7edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124340"
---
# <a name="descriptor-heaps-overview"></a>Información general sobre los montones de descriptores

Los montones de descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como vistas de recursos de sombreador (SRV), vistas de acceso desordenado (UAV), vistas de búfer constante (CBV) y muestreadores.

-   [El propósito de los montones de descriptores](#the-purpose-of-descriptor-heaps)
-   [Sincronización](#synchronization)
-   [Binding](#binding)
-   [Cambiar montones](#switching-heaps)
-   [Agrupaciones](#bundles)
-   [Administración](#management)
-   [Temas relacionados](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>El propósito de los montones de descriptores

El propósito principal de un montón de descriptores es abarcar la mayor parte de la asignación de memoria necesaria para almacenar las especificaciones de descriptor de los tipos de objeto a los que hacen referencia los sombreadores para el mayor tamaño posible de una ventana de representación (idealmente un marco completo de representación o más). Si una aplicación cambia las texturas que la canalización ve rápidamente desde la API, debe haber espacio en el montón de descriptores para definir tablas de descriptor sobre la marcha para cada conjunto de estado necesario. La aplicación puede optar por reutilizar definiciones si los recursos se usan de nuevo en otro objeto, por ejemplo, o simplemente asignar el espacio del montón secuencialmente a medida que cambia varios tipos de objeto.

Los montones de descriptores también permiten que los componentes de software individuales administren el almacenamiento de descriptores por separado.

Todos los montones son visibles para la CPU. La aplicación también puede solicitar qué propiedades de acceso de CPU debe tener un montón de descriptores (si hay alguna): escritura combinada, reescribición, y así sucesivamente. Las aplicaciones pueden crear tantos montones de descriptores como desee con las propiedades deseadas. Las aplicaciones siempre tienen la opción de crear montones de descriptores que están exclusivamente para fines de almacenamiento provisional sin restricciones de tamaño y copiarlos en montones de descriptores que se usan para la representación según sea necesario.

Hay algunas restricciones en lo que puede ir en el mismo montón de descriptores. Las entradas CBV, UAV y SRV pueden estar en el mismo montón de descriptores. Sin embargo, las entradas samplers no pueden compartir un montón con entradas CBV, UAV o SRV. Normalmente, hay dos conjuntos de montones de descriptores, uno para los recursos comunes y el segundo para samplers.

El uso de montones de descriptores de Direct3D 12 refleja lo que hace la mayoría del hardware de GPU, que es requerir descriptores en directo solo en montones de descriptores, o simplemente que se necesitan menos bits de direccionamiento si se usan estos montones. Direct3D 12 requiere el uso de montones de descriptores; no hay ninguna opción para colocar descriptores en cualquier lugar de la memoria.

Los montones de descriptores solo se pueden editar inmediatamente por la CPU, no hay ninguna opción para editar un montón de descriptores por la GPU.

## <a name="synchronization"></a>Sincronización

El contenido del montón de descriptores se puede cambiar antes, durante y después de grabar listas de comandos que hacen referencia a él. Sin embargo, los descriptores no se pueden cambiar, mientras que una lista de comandos enviada para su ejecución podría hacer referencia a esa ubicación, ya que esto podría invocar una condición de carrera.

## <a name="binding"></a>Enlace

Como máximo, se puede enlazar un montón combinado CBV/SRV/UAV y un montón sampler en cualquier momento. Estos montones se comparten entre los gráficos y las canalizaciones de proceso (que se describen en sus PSO).

## <a name="switching-heaps"></a>Cambiar montones

Es aceptable que una aplicación cambie los montones dentro de la misma lista de comandos o en otros distintos mediante las API [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) y [**Reset.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) En algún hardware, puede ser una operación costosa, que requiere una detención de GPU para vaciar todo el trabajo que depende del montón de descriptores enlazado actualmente. Como resultado, si se deben cambiar los montones de descriptores, las aplicaciones deben intentar hacerlo cuando la carga de trabajo de GPU es relativamente ligera, lo que puede limitar los cambios al inicio de una lista de comandos.

## <a name="bundles"></a>Agrupaciones

Con las agrupaciones, solo puede haber una llamada al método [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) y el conjunto de montones del descriptor debe coincidir exactamente con los de la lista de comandos que llama a la agrupación. Si la agrupación no cambia las tablas de descriptores, no es necesario establecer los montones de descriptores.

Para obtener una lista de llamadas API que no se pueden usar con agrupaciones, consulte Creación y grabación de listas de [comandos y agrupaciones.](recording-command-lists-and-bundles.md)

## <a name="management"></a>Administración

Para representar todos los objetos de una escena, se necesitan muchos descriptores y se pueden seguir algunas estrategias de administración diferentes.

La estrategia más básica sería rellenar un área nueva del montón de descriptores con todos los requisitos para la siguiente llamada a draw. Por lo tanto, justo antes de emitir la llamada a draw en la lista de comandos, se establecería un puntero de tabla descriptor en el inicio de la tabla recién rellenada. El inconveniente es que no es necesario registrar dónde se encuentra ningún descriptor determinado en el montón.

El inconveniente de esta estrategia es que podría haber una gran cantidad de repeticiones de descriptores en el montón de descriptores, especialmente cuando se representa una escena muy similar y ese espacio del montón de descriptores se va a usar rápidamente. Los montones de descriptores independientes para los que se representan en la GPU y para los que se registran mediante la CPU, probablemente serían necesarios para evitar conflictos. Como alternativa, se podría usar un sistema de subatribución.

Además, el sistema básico podría optimizarse aún más si se usan cuidadosamente tablas descriptoras superpuestas de una llamada a draw a la siguiente, de modo que solo se agregan los nuevos descriptores necesarios.

Una estrategia más eficaz que la básica sería rellenar previamente los montones de descriptores con descriptores necesarios para los objetos (o materiales) que se sabe que forman parte de la escena. La idea aquí es que solo es necesario establecer la tabla de descriptores en tiempo de dibujo, ya que el montón del descriptor se rellena con antelación.

Una variación de la estrategia de relleno previo es tratar el montón de descriptores como una matriz enorme, que contiene todos los descriptores necesarios en ubicaciones conocidas fijas. A continuación, la llamada a draw solo necesita recibir un conjunto de constantes que son los índices en la matriz de donde se deben usar los descriptores.

Una optimización adicional es asegurarse de que las constantes raíz y los descriptores raíz contienen las que cambian con más frecuencia, en lugar de colocar constantes en el montón de descriptores. Para la mayoría del hardware, se trata de una manera eficaz de controlar las constantes.

En la práctica, un motor gráfico podría usar una estrategia diferente en situaciones diferentes y combinar elementos de cada estrategia para satisfacer los requisitos de dibujo concretos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




