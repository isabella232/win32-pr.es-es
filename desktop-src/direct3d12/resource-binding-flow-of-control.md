---
title: Información general sobre el enlace de recursos
description: La clave para el enlace de recursos en DirectX 12 son los conceptos de un descriptor, las tablas de descriptores, los montones de descriptores y una firma raíz.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc7e78255c123777716eddb43d9443e19113b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103761"
---
# <a name="resource-binding-overview"></a>Información general sobre el enlace de recursos

La clave para el enlace de recursos en DirectX 12 son los conceptos de un *descriptor*, *las tablas de descriptores*, los *montones de descriptores* y una *firma raíz*.

-   [Recursos y la canalización de gráficos](#resources-and-the-graphics-pipeline)
-   [Tipos de recursos y vistas](#resource-types-and-views)
-   [Flujo de enlace de recursos de control](#resource-binding-overview)
-   [Subasignación](#suballocation)
-   [Liberar recursos](#freeing-resources)
-   [Temas relacionados](#related-topics)

## <a name="resources-and-the-graphics-pipeline"></a>Recursos y la canalización de gráficos

Los recursos del sombreador (como texturas, tablas constantes, imágenes, búferes, etc.) no están enlazados directamente a la canalización del sombreador; en su lugar, se hace referencia a ellos a través de un *descriptor*. Un descriptor es un objeto pequeño que contiene información sobre un recurso.

Los descriptores se agrupan en *tablas de descriptores* de formulario. Cada tabla de descriptores almacena información sobre un intervalo de tipos de recursos. Hay muchos tipos diferentes de recursos. Los recursos más comunes son:

-   Vistas de búfer de constantes (CBVs)
-   Vistas de acceso desordenado (UAVs)
-   Vistas de recursos del sombreador (SRVs)
-   Muestras

Los descriptores SRV, UAV y CBVs se pueden combinar en la misma tabla de descriptores.

Las canalizaciones de gráficos y de cálculo obtienen acceso a los recursos haciendo referencia a las tablas de descriptores por índice.

Las tablas de descriptor se almacenan en un *montón de descriptores*. Idealmente, los montones de descriptor contendrán todos los descriptores (en las tablas de descriptores) de uno o varios fotogramas que se van a representar. Todos los recursos se almacenarán en montones de modo de usuario.

Otro concepto es el de una *firma raíz*. La firma raíz es una Convención de enlace, definida por la aplicación, que usan los sombreadores para localizar los recursos a los que necesitan tener acceso. La firma raíz puede almacenar:

-   Índices para descriptor tablas en un montón de descriptores, donde el diseño de la tabla de descriptores se ha definido previamente.
-   Constantes, por lo que las aplicaciones pueden enlazar constantes definidas por el usuario (conocidas como *constantes raíz*) directamente a los sombreadores sin tener que ir a través de descriptores y tablas de descriptores.
-   Un número muy pequeño de descriptores directamente dentro de la firma raíz, como una vista de búfer de constantes (CBV) que cambia por dibujo, lo que evita que la aplicación tenga que colocar los descriptores en un montón de descriptores.

En otras palabras, la firma raíz proporciona optimizaciones de rendimiento adecuadas para pequeñas cantidades de datos que cambian por dibujo.

El diseño de Direct3D 12 para el enlace lo separa de otras tareas, como la administración de memoria, la administración de la duración de los objetos, el seguimiento de estado y la sincronización de memoria (consulte [las diferencias en el modelo de enlace de Direct3D 11](binding-model.md)). El enlace de Direct3D 12 está diseñado para ser de baja sobrecarga y está optimizado para las llamadas de API que se realizan con mayor frecuencia. También es escalable a través de hardware de low-end y High-End, y es escalable desde más antiguo (la canalización Direct3D 11 más lineal) hasta los enfoques más recientes (más paralelos) a la programación del motor de gráficos.

## <a name="resource-types-and-views"></a>Tipos de recursos y vistas

Los tipos de recursos son los mismos que los de Direct3D 11, es decir:

-   Texture1D y Texture1DArray
-   Texture2D y Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Búferes (tipos, estructurados y sin formato)

Las vistas de recursos son similares, pero son ligeramente diferentes de las vistas de Direct3D 11, vértices e índices que se han agregado.

-   Vista de búfer de constantes (CBV)
-   Vista de acceso desordenado (UAV)
-   Vista de recursos del sombreador (SRV)
-   Muestras
-   Vista de destino de representación (RTV)
-   Vista de galería de símbolos de profundidad (DSV)
-   Vista de búfer de índice (IBV)
-   Vista de búfer de vértices (VBV)
-   Vista de salida de flujo (SOV)

Solo las cuatro primeras de estas vistas son realmente visibles para los sombreadores, consulte [montones de descriptor visibles del sombreador](shader-visible-descriptor-heaps.md) y [montones de descriptor visibles de no sombreador](non-shader-visible-descriptor-heaps.md).

## <a name="resource-binding-flow-of-control"></a>Flujo de enlace de recursos de control

Centrándose solo en las firmas raíz, los descriptores raíz, las constantes raíz, las tablas de descriptores y los montones de descriptores, el flujo de la lógica de representación de una aplicación debe ser similar al siguiente:

-   Cree uno o más objetos de firma raíz: uno para cada configuración de enlace diferente que necesite la aplicación.
-   Cree sombreadores y estado de canalización con los objetos de firma raíz que se usarán con.
-   Cree uno (o, si es necesario, más) montones de descriptores que contendrá todos los descriptores SRV, UAV y CBV para cada fotograma de representación.
-   Inicialice los montones de descriptor con descriptores siempre que sea posible para los conjuntos de descriptores que se reutilizarán en muchos fotogramas.
-   Para cada fotograma que se va a representar:
    -   Para cada lista de comandos:
        -   Establezca la firma raíz actual que se va a usar (y cámbielo si es necesario durante la representación, lo que rara vez es necesario).
        -   Actualice algunas constantes y/o descriptores de la firma raíz de la firma raíz para la nueva vista (como las proyecciones de mundo o vista).
        -   Para cada elemento que se va a dibujar:
            -   Defina los nuevos descriptores en los montones de descriptores según sea necesario para la representación por objeto. En el caso de los montones de descriptor visibles del sombreador, la aplicación debe asegurarse de usar el espacio del montón del descriptor al que ya no se hace referencia mediante la representación que podría estar en vuelo; por ejemplo, asignar espacio linealmente a través del montón del descriptor durante la representación.
            -   Actualice la firma raíz con punteros a las regiones necesarias de los montones de descriptor. Por ejemplo, una tabla de descriptores podría señalar a algunos descriptores estáticos (sin cambiar) inicializados anteriormente, mientras que otra tabla de descriptores podría señalar a algunos descriptores dinámicos configurados para la representación actual.
            -   Actualice algunas constantes y/o descriptores de la firma raíz para la representación por elemento.
            -   Establezca el estado de canalización para el elemento que se va a dibujar (solo si el cambio es necesario), compatible con la firma raíz enlazada actualmente.
            -   Dibujar
        -   Repetir (elemento siguiente)
    -   Repetir (lista de comandos siguiente)
    -   Estrictamente cuando la GPU haya terminado con cualquier memoria que ya no se vaya a utilizar, se puede liberar. No es necesario eliminar las referencias de descriptores a ella si no se envía ninguna representación adicional que use esos descriptores. Por lo tanto, la representación subsiguiente puede apuntar a otras áreas de los montones de descriptores, o bien se pueden sobrescribir descriptores obsoletos con descriptores válidos para reutilizar el espacio del montón del descriptor.
-   Repetir (fotograma siguiente)

Tenga en cuenta que otros tipos de descriptores, vistas de destino de representación (RTVs), vistas de estarcido de profundidad (DSV), vistas de búfer de índice (IBVs), vistas de búfer de vértices (VBVs) y vistas de objeto de sombreador (SOV), se administran de forma diferente. El controlador controla el control de versiones del conjunto de descriptores enlazado para cada dibujo durante la grabación de la lista de comandos (de forma similar al modo en que el hardware o el controlador controlan la versión de los enlaces de la firma raíz). Esto no es lo mismo que el contenido de los montones de descriptor visibles del sombreador, para los que la aplicación debe asignar manualmente a través del montón, ya que hace referencia a distintos descriptores entre los dibujos. El control de versiones del contenido del montón que es sombreador-visible se deja a la aplicación porque permite que las aplicaciones realicen tareas como reutilizar descriptores que no cambian, también se usan conjuntos estáticos grandes de descriptores y se usa la indización de sombreador (por ejemplo, por identificador de material) para seleccionar los descriptores que se van a usar en el montón de descriptores o para usar combinaciones de técnicas para diferentes conjuntos de descriptores. El hardware no está equipado para controlar este tipo de flexibilidad para los demás tipos de descriptores (RTV, DSV, IBV, VBV, SOV).

## <a name="suballocation"></a>Subasignación

En Direct3D 12, la aplicación tiene un control de bajo nivel sobre la administración de memoria. En versiones anteriores de Direct3D, incluido Direct3D 11, hubiera una asignación por recurso. En Direct3D 12, la aplicación puede usar la API para asignar un gran bloque de memoria, más grande de lo que necesitaría un solo objeto. Una vez hecho esto, la aplicación puede crear descriptores para apuntar a las secciones de ese bloque de memoria grande. Este proceso consiste en decidir qué colocar (bloques más pequeños dentro del bloque grande) se denomina *subasignación*. Habilitar la aplicación para hacer esto puede producir mejoras en el uso eficaz de la memoria y el cálculo. Por ejemplo, el cambio de nombre de recursos se representa obsoleto. En lugar de esto, las aplicaciones pueden usar vallas para determinar cuándo se usa un recurso determinado y cuándo no se especifican en las ejecuciones de la lista de comandos donde la lista de comandos requiere el uso de ese recurso en particular.

## <a name="freeing-resources"></a>Liberar recursos

Antes de que se pueda liberar cualquier memoria enlazada a la canalización, la GPU debe terminar con ella.

Esperar a que la representación de fotogramas sea probablemente la forma más amplia de asegurarse de que la GPU ha finalizado. En un grano más preciso, puede volver a usar las barreras: cuando un comando se grabe en una lista de comandos en la que desee realizar un seguimiento de la finalización, inserte una barrera inmediatamente después. A continuación, puede realizar varias operaciones de sincronización con la barrera. Puede enviar nuevo trabajo (listas de comandos) que espera hasta que se ha pasado una barrera especificada en la GPU, lo que indica que todo antes de que se complete, o bien puede solicitar que se genere un evento de CPU cuando se haya superado la barrera (que la aplicación puede estar esperando en un subproceso en espera). En Direct3D 11, este era `EnqueueSetEvent` ().

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace de recursos](resource-binding.md)
</dt> </dl>

 

 




