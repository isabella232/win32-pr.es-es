---
title: Información general sobre montones de descriptores
description: Los montones descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bf720ebb71d016457fa4383a8d33aa62e2eee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103673"
---
# <a name="descriptor-heaps-overview"></a>Información general sobre montones de descriptores

Los montones descriptores contienen muchos tipos de objetos que no forman parte de un objeto de estado de canalización (PSO), como las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores.

-   [El propósito de los montones de descriptor](#the-purpose-of-descriptor-heaps)
-   [Sincronización](#synchronization)
-   [Binding](#binding)
-   [Cambiar montones](#switching-heaps)
-   [Agrupaciones](#bundles)
-   [Administración](#management)
-   [Temas relacionados](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>El propósito de los montones de descriptor

El propósito principal de un montón de descriptores es abarcar la asignación de memoria masiva necesaria para almacenar las especificaciones de descriptor de tipos de objeto a los que los sombreadores hacen referencia para el tamaño de una ventana de representación lo más grande posible (lo ideal es un marco completo de representación o más). Si una aplicación está cambiando las texturas que la canalización ve rápidamente desde la API, debe haber espacio en el montón de descriptores para definir las tablas de descriptor sobre la marcha para cada conjunto de Estados necesarios. La aplicación puede optar por reutilizar definiciones si los recursos se utilizan de nuevo en otro objeto, por ejemplo, o simplemente asignan el espacio del montón secuencialmente a medida que cambia varios tipos de objeto.

Los montones de descriptor también permiten a los componentes de software individuales administrar el almacenamiento de descriptores de forma independiente entre sí.

Todos los montones están visibles para la CPU. La aplicación también puede solicitar las propiedades de acceso a la CPU que debe tener un montón de descriptores (si existen): escritura combinada, escritura inversa, etc. Las aplicaciones pueden crear tantos montones de descriptor como sea necesario, con las propiedades que desee. Las aplicaciones siempre tienen la opción de crear montones de descriptor que son exclusivamente para fines de almacenamiento provisional sin restricciones de tamaño, y copiar en montones de descriptores que se usan para la representación según sea necesario.

Hay algunas restricciones en lo que puede ir en el mismo montón de descriptores. Las entradas CBV, UAV y SRV pueden estar en el mismo montón de descriptores. Sin embargo, las entradas de muestreadores no pueden compartir un montón con las entradas CBV, UAV o SRV. Normalmente, hay dos conjuntos de montones de descriptor, uno para los recursos comunes y el segundo para los muestreadores.

El uso de montones de descriptor de Direct3D 12 refleja lo que hace la mayoría del hardware de GPU, que es requerir descriptores en vivo solo en montones de descriptores, o simplemente que se necesitan menos bits de direccionamiento si se usan estos montones. Direct3D 12 requiere el uso de montones de descriptor, no hay ninguna opción para colocar los descriptores en cualquier parte de la memoria.

Los montones de descriptor solo se pueden editar inmediatamente mediante la CPU, no hay ninguna opción para editar un montón de descriptores en la GPU.

## <a name="synchronization"></a>Synchronization

El contenido del montón descriptor se puede cambiar antes, durante y después de grabar las listas de comandos que hacen referencia a él. Sin embargo, los descriptores no se pueden cambiar mientras una lista de comandos enviada para su ejecución puede hacer referencia a esa ubicación, ya que esto podría invocar una condición de carrera.

## <a name="binding"></a>Enlace

Como máximo, un montón combinado CBV/SRV/UAV y un montón de muestra se pueden enlazar al mismo tiempo. Estos montones se comparten entre las canalizaciones de gráficos y de proceso (descritas en su PSO).

## <a name="switching-heaps"></a>Cambiar montones

Es aceptable que una aplicación cambie los montones dentro de la misma lista de comandos o en otros diferentes mediante las API [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) y [**RESET**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) . En algunos requisitos de hardware, esto puede ser una operación costosa, que requiere una detención de GPU para vaciar todo el trabajo que depende del montón de descriptor enlazado actualmente. Como resultado, si se deben cambiar los montones de descriptor, las aplicaciones deben intentar hacerlo cuando la carga de trabajo de la GPU sea relativamente ligera, lo que puede limitar los cambios al inicio de una lista de comandos.

## <a name="bundles"></a>Agrupaciones

Con las agrupaciones solo puede haber una llamada al método [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) , y el conjunto de montones descriptores debe coincidir exactamente con los de la lista de comandos que llama a la agrupación. Si el paquete no cambia las tablas de descriptores, no es necesario establecer los montones de descriptor.

Para obtener una lista de llamadas API que no se pueden usar con agrupaciones, consulte [crear y grabar listas de comandos y agrupaciones](recording-command-lists-and-bundles.md).

## <a name="management"></a>Administración

Para representar todos los objetos de una escena, se necesitarán muchos descriptores y se pueden seguir algunas estrategias de administración diferentes.

La estrategia más básica sería rellenar una nueva área del montón descriptor con todos los requisitos para la siguiente llamada a Draw. Por lo tanto, justo antes de emitir la llamada a Draw en la lista de comandos, un puntero de tabla de descriptores se establecería en el inicio de la tabla recién rellenada. El lado es que no es necesario registrar dónde se encuentra un descriptor determinado en el montón.

El inconveniente de esta estrategia es que podría haber una gran cantidad de repeticiones de descriptores en el montón de descriptores, especialmente cuando se está representando una escena muy similar y el espacio de montón del descriptor se va a usar rápidamente. Los montones de descriptor independientes para los que se representan en la GPU y para los que se registran con la CPU, probablemente serán necesarios para evitar conflictos. También se podría usar un sistema de subasignación.

Además, el sistema básico se podría optimizar aún más mediante el uso minucioso de las tablas de descriptores superpuestas de una llamada a Draw a la siguiente, de modo que solo se agreguen los nuevos descriptores.

Una estrategia más eficaz que la básica sería rellenar previamente los montones de descriptor con los descriptores necesarios para los objetos (o materiales) que se sabe que forman parte de la escena. La idea es que solo es necesario establecer la tabla de descriptores en el momento de la hora de dibujo, ya que el montón de descriptores se rellena con anterioridad.

Una variación de la estrategia de prerelleno consiste en tratar el montón de descriptores como una gran matriz, que contiene todos los descriptores necesarios en ubicaciones conocidas fijas. A continuación, la llamada a Draw solo tiene que recibir un conjunto de constantes que son los índices en la matriz de donde se deben usar los descriptores.

Una optimización adicional consiste en asegurarse de que las constantes raíz y los descriptores raíz contengan los que cambian con más frecuencia, en lugar de colocar constantes en el montón de descriptores. Para la mayoría del hardware, se trata de una forma eficaz de controlar las constantes.

En la práctica, un motor de gráficos podría usar una estrategia diferente en situaciones diferentes y combinar elementos de cada estrategia para satisfacer los requisitos de dibujo concretos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




