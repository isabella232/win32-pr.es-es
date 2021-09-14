---
title: Cambios importantes en Direct3D 12 respecto de Direct3D 11
description: Direct3D 12 representa una salida significativa del modelo de programación de Direct3D 11. Direct3D 12 permite que las aplicaciones se acerquen más al hardware que nunca.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be891d71d6c1f3a12d8d5aac3ec46785207ed31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072966"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Cambios importantes en Direct3D 12 respecto de Direct3D 11

Direct3D 12 representa una salida significativa del modelo de programación de Direct3D 11. Direct3D 12 permite que las aplicaciones se acerquen más al hardware que nunca. Al estar más cerca del hardware, Direct3D 12 es más rápido y eficaz. Sin embargo, el hecho de que la aplicación tenga mayor velocidad y eficacia con Direct3D 12 es que usted es responsable de más tareas de las que tenía con Direct3D 11.

-   [Sincronización explícita](#explicit-synchronization)
-   [Administración de residencia de memoria física](#physical-memory-residency-management)
-   [Objetos de estado de canalización](#pipeline-state-objects)
-   [Listas de comandos y agrupaciones](#command-lists-and-bundles)
-   [Montones y tablas de descriptores](#descriptor-heaps-and-tables)
-   [Porte desde Direct3D 11](#porting-from-direct3d-11)
-   [Temas relacionados](#related-topics)

Direct3D 12 es una vuelta a la programación de bajo nivel; proporciona más control sobre los elementos gráficos de los juegos y las aplicaciones mediante la introducción de estas nuevas características: objetos para representar el estado general de la canalización, listas de comandos y agrupaciones para el envío de trabajos, y montones y tablas de descriptores para el acceso a los recursos.

La aplicación ha aumentado la velocidad y la eficacia con Direct3D 12, pero usted es responsable de más tareas que con Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronización explícita

-   En Direct3D 12, la sincronización de CPU y GPU es ahora la responsabilidad explícita de la aplicación y ya no la realiza implícitamente el tiempo de ejecución, como en Direct3D 11. Este hecho también significa que Direct3D 12 no realiza ninguna comprobación automática de los riesgos de canalización, por lo que de nuevo esta es la responsabilidad de las aplicaciones.
-   En Direct3D 12, las aplicaciones son responsables de canalizar las actualizaciones de datos. Es decir, el patrón "Map/Lock-DISCARD" de Direct3D 11 debe realizarse manualmente en Direct3D 12. En Direct3D 11, si la GPU sigue usando el búfer al llamar a [**ID3D11DeviceContext::Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) with [**D3D11 \_ MAP WRITE \_ \_ DISCARD**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map), el tiempo de ejecución devuelve un puntero a una nueva región de memoria en lugar de los datos antiguos del búfer. Esto permite que la GPU siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; El búfer antiguo se reutiliza o destruye automáticamente cuando la GPU termina con él.
-   En Direct3D 12, la aplicación controla explícitamente todas las actualizaciones dinámicas (incluidos los búferes constantes, los búferes de vértices dinámicos, las texturas dinámicas, entre otras). Estas actualizaciones dinámicas incluyen las barreras de GPU o el almacenamiento en búfer necesarios. La aplicación es responsable de mantener la memoria disponible hasta que ya no sea necesaria.
-   Direct3D 12 usa el recuento de referencias de estilo COM solo para las duraciones de las interfaces (mediante el uso del modelo de referencia débil de Direct3D vinculado a la duración del dispositivo). Todas las duraciones de memoria de recursos y de descripción son la única responsabilidad de la aplicación que se debe mantener durante el tiempo adecuado y no se cuentan las referencias. Direct3D 11 usa el recuento de referencias para administrar también la duración de las dependencias de interfaz.

## <a name="physical-memory-residency-management"></a>Administración de residencia de memoria física

Una aplicación direct3D 12 debe evitar las condiciones de carrera entre varias colas, varios adaptadores y los subprocesos de CPU. D3D12 ya no sincroniza la CPU y la GPU, ni admite mecanismos cómodos para cambiar el nombre de los recursos o el almacenamiento en búfer múltiple. Las barreras deben usarse para evitar que varias unidades de procesamiento sobrescriba memoria antes de que otra unidad de procesamiento termine de usarlo.

La aplicación Direct3D 12 debe asegurarse de que los datos residen en la memoria mientras la GPU los lee. La memoria utilizada por cada objeto se hace residentes durante la creación del objeto. Las aplicaciones que llaman a estos métodos deben usar barreras para asegurarse de que la GPU no tiene acceso a los objetos que se han expulsado.

Las barreras de recursos son otro tipo de sincronización necesaria, que se usa para sincronizar las transiciones de recursos y recursos en un nivel muy granular.

Consulte Administración [de memoria en Direct3D 12.](memory-management.md)

## <a name="pipeline-state-objects"></a>Objetos de estado de canalización

Direct3D 11 permite la manipulación del estado de canalización a través de un gran conjunto de objetos independientes. Por ejemplo, el estado del ensamblador de entrada, el estado del sombreador de píxeles, el estado del rasterizador y el estado de fusión de salida se pueden modificar de forma independiente. Este diseño proporciona una representación cómoda y relativamente de alto nivel de la canalización de gráficos, pero no utiliza las funcionalidades del hardware moderno, principalmente porque los distintos estados suelen ser interdependientes. Por ejemplo, muchas GPU combinan el estado de fusión de salida y sombreador de píxeles en una única representación de hardware. Sin embargo, dado que la API de Direct3D 11 permite que estas fases de canalización se establezcan por separado, el controlador de pantalla no puede resolver problemas de estado de canalización hasta que se haya finalizado el estado, lo que no es hasta el momento del dibujo. Este esquema retrasa la configuración del estado de hardware, lo que significa una sobrecarga adicional y menos llamadas de dibujo máximas por fotograma.

Direct3D 12 aborda este esquema mediante la unificación de gran parte del estado de canalización en objetos de estado de canalización (PSO) inmutables, que se finalizarán tras la creación. A continuación, el hardware y los controladores pueden convertir inmediatamente el PSO en las instrucciones nativas de hardware y el estado necesarios para ejecutar el trabajo de GPU. Todavía puede cambiar dinámicamente qué PSO está en uso, pero para ello, el hardware solo necesita copiar la cantidad mínima de estado calculado previamente directamente en los registros de hardware, en lugar de calcular el estado de hardware sobre la marcha. Mediante el uso de PSO, la sobrecarga de las llamadas a draw se reduce significativamente y pueden producirse muchas más llamadas a draw por fotograma. Para obtener más información sobre los PSO, consulte Administración del estado de canalización [de gráficos en Direct3D 12.](managing-graphics-pipeline-state-in-direct3d-12.md)

## <a name="command-lists-and-bundles"></a>Listas de comandos y agrupaciones

En Direct3D 11, todo el envío de trabajo se realiza a través del contexto inmediato [,](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render)que representa una sola secuencia de comandos que van a la GPU. Para lograr el escalado multiproceso, los juegos también [tienen contextos diferidos](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) disponibles. Los contextos diferidos de Direct3D 11 no se asignan perfectamente al hardware, por lo que se puede hacer relativamente poco trabajo en ellos.

Direct3D 12 presenta un nuevo modelo para el envío de trabajo basado en listas de comandos que contienen la totalidad de la información necesaria para ejecutar una carga de trabajo determinada en la GPU. Cada nueva lista de comandos contiene información como qué PSO usar, qué recursos de textura y búfer son necesarios y los argumentos para todas las llamadas a draw. Dado que cada lista de comandos es independiente y no hereda ningún estado, el controlador puede calcular previamente todos los comandos de GPU necesarios por adelantado y de forma libre. El único proceso serie necesario es el envío final de listas de comandos a la GPU a través de la cola de comandos.

Además de las listas de comandos, Direct3D 12 también presenta un segundo nivel de cálculo previo del trabajo: *agrupa*. A diferencia de las listas de comandos, que son completamente independientes y normalmente se construyen, se envían una vez y se descartan, los paquetes proporcionan una forma de herencia de estado que permite la reutilización. Por ejemplo, si un juego quiere dibujar dos modelos de caracteres con texturas diferentes, un enfoque es registrar una lista de comandos con dos conjuntos de llamadas a draw idénticas. Pero otro enfoque es "grabar" un conjunto que dibuje un modelo de caracteres único y, a continuación, "reproducir" el lote dos veces en la lista de comandos mediante recursos diferentes. En el último caso, el controlador para mostrar solo tiene que calcular las instrucciones adecuadas una vez y la creación de la lista de comandos equivale básicamente a dos llamadas de función de bajo costo.

Para obtener más información sobre las listas de comandos y los paquetes, vea [Envío de trabajo en Direct3D 12.](command-queues-and-command-lists.md)

## <a name="descriptor-heaps-and-tables"></a>Montones y tablas de descriptores

El enlace de recursos en Direct3D 11 es muy abstracto y cómodo, pero deja muchas funcionalidades de hardware modernas infrautilizadas. En Direct3D 11,  los juegos crean objetos de  vista de recursos y, a continuación, enlazan esas vistas a varias ranuras en varias fases del sombreador de la canalización. Los sombreadores, a su vez, leen datos de esas ranuras de enlace explícitas, que se fijan en tiempo de dibujo. Este modelo significa que cada vez que un juego se dibuja con recursos diferentes, debe volver a enlazar distintas vistas a ranuras diferentes y llamar a draw de nuevo. Este caso también representa la sobrecarga que se puede eliminar mediante el uso completo de funcionalidades de hardware modernas.

Direct3D 12 cambia el modelo de enlace para que coincida con el hardware moderno y mejora significativamente el rendimiento. En lugar de requerir vistas de recursos independientes y asignación explícita a ranuras, Direct3D 12 proporciona un montón de descriptores en el que los juegos crean sus distintas vistas de recursos. Este esquema proporciona un mecanismo para que la GPU escriba directamente la descripción del recurso nativo del hardware (descriptor) en la memoria por adelantado. Para declarar qué recursos va a usar la canalización para una llamada a draw determinada, los juegos especifican una o varias tablas de descriptores que representan los sub intervalos del montón de descriptores completos. Como el montón de descriptores ya se ha rellenado con los datos de descriptor específicos del hardware adecuados, cambiar las tablas de descriptores es una operación de muy bajo costo.

Además del rendimiento mejorado que ofrecen los montones de descriptores y las tablas, Direct3D 12 también permite que los recursos se indexen dinámicamente en sombreadores, lo que proporciona una flexibilidad sin precedentes y desbloquea nuevas técnicas de representación. Por ejemplo, los motores de representación diferida modernos suelen codificar un identificador de material u objeto de algún tipo en el búfer g intermedio. En Direct3D 11, estos motores deben tener cuidado para evitar el uso de demasiados materiales, ya que incluir demasiados en un búfer g puede ralentizar significativamente el paso de representación final. Con los recursos indexables dinámicamente, una escena con mil materiales se puede finalizar tan rápidamente como una con solo diez.

Para obtener más información sobre los montones de descriptores y las tablas, vea [Enlace](resource-binding.md)de recursos y Diferencias en el modelo de enlace [de Direct3D 11.](binding-model.md)

## <a name="porting-from-direct3d-11"></a>Porte desde Direct3D 11

La porción desde Direct3D 11 es un proceso implicado, descrito en [Porting from Direct3D 11 to Direct3D 12 ( Portear de Direct3D 11 a Direct3D 12).](porting-from-direct3d-11-to-direct3d-12.md) Consulte también el intervalo de opciones de Trabajar con [Direct3D 11, Direct3D 10 y Direct2D.](direct3d-12-interop.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 