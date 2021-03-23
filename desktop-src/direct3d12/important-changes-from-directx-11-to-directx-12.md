---
title: Cambios importantes de Direct3D 11 a Direct3D 12
description: Direct3D 12 representa una salida significativa del modelo de programación de Direct3D 11. Direct3D 12 permite que las aplicaciones se acerquen más al hardware que nunca.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be891d71d6c1f3a12d8d5aac3ec46785207ed31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549082"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Cambios importantes de Direct3D 11 a Direct3D 12

Direct3D 12 representa una salida significativa del modelo de programación de Direct3D 11. Direct3D 12 permite que las aplicaciones se acerquen más al hardware que nunca. Al estar más cerca del hardware, Direct3D 12 es más rápido y eficaz. Sin embargo, el equilibrio entre la aplicación y la mayor velocidad y eficacia con Direct3D 12 es que usted es responsable de realizar más tareas de las que tenía Direct3D 11.

-   [Sincronización explícita](#explicit-synchronization)
-   [Administración de la residencia de memoria física](#physical-memory-residency-management)
-   [Objetos de estado de canalización](#pipeline-state-objects)
-   [Listas de comandos y agrupaciones](#command-lists-and-bundles)
-   [Tablas y montones de descriptores](#descriptor-heaps-and-tables)
-   [Portabilidad desde Direct3D 11](#porting-from-direct3d-11)
-   [Temas relacionados](#related-topics)

Direct3D 12 es una devolución a la programación de bajo nivel; proporciona un mayor control sobre los elementos gráficos de los juegos y las aplicaciones mediante la introducción de estas nuevas características: objetos para representar el estado general de la canalización, las listas de comandos y las agrupaciones para el envío del trabajo, y las tablas y los montones de descriptor para el acceso a los recursos.

La aplicación ha aumentado la velocidad y la eficacia con Direct3D 12, pero usted es responsable de realizar más tareas de las que tenía Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronización explícita

-   En Direct3D 12, la sincronización de CPU-GPU es ahora la responsabilidad explícita de la aplicación y ya no la realiza el tiempo de ejecución de forma implícita, como en Direct3D 11. Este hecho también significa que Direct3D 12 no realiza la comprobación automática de los peligros de la canalización, por lo que es responsabilidad de las aplicaciones.
-   En Direct3D 12, las aplicaciones son responsables de la canalización de las actualizaciones de datos. Es decir, el patrón "Map/Lock-discard" de Direct3D 11 debe realizarse manualmente en Direct3D 12. En Direct3D 11, si la GPU todavía usa el búfer cuando se llama a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) con [**D3D11 \_ map \_ Write \_ discard**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map), el tiempo de ejecución devuelve un puntero a una nueva región de memoria en lugar de los datos de búfer antiguos. Esto permite que la GPU siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; el búfer antiguo se reutiliza o se destruye automáticamente cuando la GPU finaliza con él.
-   En Direct3D 12, todas las actualizaciones dinámicas (incluidos los búferes de constantes, los búferes de vértices dinámicos, las texturas dinámicas, etc.) son controladas explícitamente por la aplicación. Estas actualizaciones dinámicas incluyen las barreras o el almacenamiento en búfer necesarios de la GPU. La aplicación es responsable de mantener la memoria disponible hasta que ya no se necesita.
-   Direct3D 12 usa el recuento de referencias de estilo COM solo para las duraciones de las interfaces (mediante el modelo de referencia débil de Direct3D vinculado a la duración del dispositivo). Toda la duración de la memoria de los recursos y las descripciones es el único responsable de la aplicación para mantener la duración adecuada y no se cuentan las referencias. Direct3D 11 usa el recuento de referencias para administrar también la duración de las dependencias de la interfaz.

## <a name="physical-memory-residency-management"></a>Administración de la residencia de memoria física

Una aplicación de Direct3D 12 debe evitar las condiciones de carrera entre varias colas, varios adaptadores y los subprocesos de CPU. D3D12 ya no sincroniza la CPU y la GPU, ni admite mecanismos cómodos para el cambio de nombre de recursos o el almacenamiento en búfer múltiple. Las barreras deben usarse para evitar que varias unidades de procesamiento sobrescriban la memoria antes de que otra unidad de procesamiento termine de usarlas.

La aplicación Direct3D 12 debe asegurarse de que los datos residen en la memoria mientras la GPU lo lee. La memoria usada por cada objeto se hace residente durante la creación del objeto. Las aplicaciones que llaman a estos métodos deben usar barreras para asegurarse de que la GPU no tenga acceso a los objetos que se han expulsado.

Las barreras de recursos son otro tipo de sincronización necesario, que se utiliza para sincronizar las transiciones de recursos y Subrecursos en un nivel muy granular.

Consulte [Administración de memoria en Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Objetos de estado de canalización

Direct3D 11 permite la manipulación del estado de la canalización a través de un gran conjunto de objetos independientes. Por ejemplo, el estado del ensamblador de entrada, el estado del sombreador de píxeles, el estado de rasterizador y el estado de fusión de salida se pueden modificar de forma independiente. Este diseño proporciona una representación práctica y relativamente de alto nivel de la canalización de gráficos, pero no utiliza las capacidades del hardware moderno, principalmente porque los diversos Estados suelen ser interdependientes. Por ejemplo, muchas GPU combinan el sombreador de píxeles y el estado de fusión de salida en una única representación de hardware. Sin embargo, dado que la API de Direct3D 11 permite que estas fases de canalización se establezcan por separado, el controlador de pantalla no puede resolver los problemas de estado de la canalización hasta que finalice el estado, que no es hasta el momento de la hora de dibujo. Este esquema retrasa la configuración de estado de hardware, lo que significa sobrecarga adicional y menos llamadas de dibujo por fotograma.

Direct3D 12 aborda este esquema al unificar gran parte del estado de la canalización en objetos de estado de canalización inmutables (PSO), que se finalizan tras la creación. El hardware y los controladores pueden convertir inmediatamente el PSO en cualquier Estado y instrucciones nativas de hardware necesarias para ejecutar el trabajo de la GPU. Todavía puede cambiar dinámicamente qué PSO está en uso, pero para hacerlo, el hardware solo necesita copiar la cantidad mínima de estado precalculada directamente en los registros de hardware, en lugar de calcular el estado del hardware sobre la marcha. Mediante el uso de PSO, la sobrecarga de la llamada a Draw se reduce significativamente y se pueden producir muchas más llamadas a Draw por fotograma. Para obtener más información sobre PSO, vea [administrar el estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Listas de comandos y agrupaciones

En Direct3D 11, todo el envío de trabajo se realiza a través del [contexto inmediato](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), que representa una única secuencia de comandos que van a la GPU. Para lograr el escalado multiproceso, los juegos también tienen [contextos diferidos](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) a su disposición. Los contextos aplazados en Direct3D 11 no se asignan perfectamente al hardware, por lo que se puede hacer relativamente poco trabajo en ellos.

Direct3D 12 presenta un nuevo modelo para el envío de trabajo basado en listas de comandos que contienen toda la información necesaria para ejecutar una carga de trabajo determinada en la GPU. Cada nueva lista de comandos contiene información como qué PSO usar, qué recursos de textura y de búfer son necesarios y los argumentos para todas las llamadas a Draw. Dado que cada lista de comandos es independiente y no hereda ningún Estado, el controlador puede calcular previamente todos los comandos de GPU necesarios por adelantado y de forma libre. El único proceso en serie necesario es el envío final de las listas de comandos a la GPU a través de la cola de comandos.

Además de las listas de comandos, Direct3D 12 también presenta un segundo nivel de cálculo previo de trabajo: *paquetes*. A diferencia de las listas de comandos, que son completamente independientes y que normalmente se construyen, envían una vez y se descartan, los paquetes proporcionan una forma de herencia de estado que permite la reutilización. Por ejemplo, si un juego desea dibujar dos modelos de caracteres con distintas texturas, un enfoque consiste en registrar una lista de comandos con dos conjuntos de llamadas Draw idénticas. Pero otro enfoque es "grabar" una agrupación que dibuja un modelo de un solo carácter y, a continuación, "reproducir" el paquete dos veces en la lista de comandos con recursos diferentes. En el último caso, el controlador de pantalla solo tiene que calcular las instrucciones adecuadas una vez, y la creación de la lista de comandos básicamente se refiere a dos llamadas de función de bajo costo.

Para obtener más información sobre las listas de comandos y agrupaciones, vea [envío de trabajos en Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Tablas y montones de descriptores

El enlace de recursos en Direct3D 11 está muy condensado y práctico, pero deja muchas capacidades de hardware modernas poco utilizadas. En Direct3D 11, los juegos crean objetos de *vista* de recursos y, luego, enlazan esas vistas a varias *ranuras* en varias fases del sombreador en la canalización. Los sombreadores, a su vez, leen los datos de esas ranuras de enlace explícitas, que se corrigen en tiempo de dibujo. Este modelo significa que cada vez que un juego dibuje con distintos recursos, debe volver a enlazar diferentes vistas a diferentes ranuras y volver a llamar a Draw. Este caso también representa la sobrecarga que se puede eliminar al usar completamente las capacidades de hardware modernas.

Direct3D 12 cambia el modelo de enlace para que coincida con el hardware moderno y mejora significativamente el rendimiento. En lugar de requerir vistas de recursos independientes y la asignación explícita a las ranuras, Direct3D 12 proporciona un montón de descriptores en el que los juegos crean sus diversas vistas de recursos. Este esquema proporciona un mecanismo para que la GPU escriba directamente el hardware: Descripción de los recursos nativos (descriptor) en la memoria por adelantado. Para declarar qué recursos va a utilizar la canalización para una llamada de Draw determinada, los juegos especifican una o más tablas de descriptores que representan subintervalos del montón de descriptor completo. Dado que el montón de descriptores ya se ha rellenado con los datos de descriptor específicos del hardware adecuados, el cambio de las tablas de descriptores es una operación extremadamente económica.

Además del rendimiento mejorado que ofrecen los montones y las tablas de descriptores, Direct3D 12 también permite indexar dinámicamente los recursos en sombreadores, lo que proporciona una flexibilidad sin precedentes y desbloquea nuevas técnicas de representación. Por ejemplo, los motores de representación diferidos modernos normalmente codifican un material o un identificador de objeto de algún tipo en el búfer g intermedio. En Direct3D 11, estos motores deben tener cuidado de evitar el uso de demasiados materiales, ya que incluir demasiados en un búfer g puede ralentizar considerablemente la fase de representación final. Con recursos indexables dinámicamente, una escena con mil materiales se puede finalizar tan pronto como una con solo diez.

Para obtener más información sobre los montones y las tablas de descriptores, vea [enlace de recursos](resource-binding.md)y [diferencias en el modelo de enlace de Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Portabilidad desde Direct3D 11

La migración de Direct3D 11 es un proceso implicado, que se describe en [migración de Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md). Consulte también el intervalo de opciones para [trabajar con Direct3D 11, Direct3D 10 y Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 