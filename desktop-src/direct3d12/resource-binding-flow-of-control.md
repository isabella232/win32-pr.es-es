---
title: Introducción al enlace de recursos
description: Las claves para comprender el enlace de recursos en DirectX 12 son los conceptos de descriptores, tablas de descriptores, montones de descriptores y firmas raíz.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657e380c58182fee8ad2c82f3af0c6fdd5ffec76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072889"
---
# <a name="resource-binding-overview"></a>Introducción al enlace de recursos

Las claves para comprender el enlace de recursos en DirectX 12 son los conceptos de descriptores, tablas de descriptores, montones de descriptores y firmas raíz.

## <a name="resources-and-the-graphics-pipeline"></a>Recursos y la canalización de gráficos

Los recursos de sombreador (como texturas, tablas constantes, imágenes, búferes, entre otros) no están enlazados directamente a la canalización del sombreador. en su lugar, se hace referencia a ellos a través de *un descriptor*. Un descriptor es un objeto pequeño que contiene información sobre un recurso.

Los descriptores se agrupan para formar *tablas de descriptores.* Cada tabla de descriptores almacena información sobre un intervalo de tipos de recursos. Hay muchos tipos diferentes de recursos. Los recursos más comunes son:

-   Vistas de búfer constante (CBV)
-   Vistas de acceso no ordenado (UAV)
-   Vistas de recursos de sombreador (SRV)
-   Muestras

Los descriptores SRV, UAV y CBV se pueden combinar en la misma tabla de descriptores.

Las canalizaciones de proceso y gráficos obtienen acceso a los recursos haciendo referencia a tablas de descriptores por índice.

Las tablas de descriptores se almacenan en un *montón de descriptores.* Idealmente, los montones de descriptores contendrán todos los descriptores (en tablas de descriptores) para que se represente uno o varios fotogramas. Todos los recursos se almacenarán en montones en modo de usuario.

Otro concepto es el de una *firma raíz*. La firma raíz es una convención de enlace, definida por la aplicación, que usan los sombreadores para buscar los recursos a los que necesitan acceso. La firma raíz puede almacenar:

-   Indexa las tablas de descriptor en un montón de descriptores, donde el diseño de la tabla de descriptores se ha predefinido.
-   Constantes, por lo que las aplicaciones pueden enlazar constantes definidas por el usuario (conocidas como constantes *raíz)* directamente a sombreadores sin tener que pasar por descriptores y tablas de descriptores.
-   Un número muy pequeño de descriptores directamente dentro de la firma raíz, como una vista de búfer constante (CBV) que cambia por dibujo, lo que evita que la aplicación necesite colocar esos descriptores en un montón de descriptores.

En otras palabras, la firma raíz proporciona optimizaciones de rendimiento adecuadas para pequeñas cantidades de datos que cambian por dibujo.

El diseño de Direct3D 12 para el enlace lo separa de otras tareas, como la administración de memoria, la administración de la duración de objetos, el seguimiento de estado y la sincronización de memoria (consulte Diferencias en el modelo de enlace de [Direct3D 11).](binding-model.md) El enlace de Direct3D 12 está diseñado para ser de baja sobrecarga y optimizado para las llamadas API que se realizan con más frecuencia. También es escalable en hardware de bajo a extremo superior, y escalable desde los enfoques más antiguos (la canalización direct3D 11 más lineal) a los enfoques más recientes (más paralelos) para la programación del motor gráfico.

## <a name="resource-types-and-views"></a>Tipos de recursos y vistas

Los tipos de recursos son los mismos que los de Direct3D 11, esndo:

-   Texture1D y Texture1DArray
-   Texture2D y Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Búferes (con tipo, estructurados y sin procesar)

Las vistas de recursos son similares, pero ligeramente diferentes de Direct3D 11, y se han agregado vistas de búfer de vértices e índices.

-   Vista de búfer de constantes (CBV)
-   Vista de acceso sin ordenar (UAV)
-   Vista de recursos del sombreador (SRV)
-   Muestras
-   Vista de destino de representación (RTV)
-   Vista de galería de símbolos de profundidad (DSV)
-   Vista de búfer de índice (IBV)
-   Vista búfer de vértices (VBV)
-   Vista de salida de flujo (SOV)

Solo las cuatro primeras vistas son realmente visibles para los sombreadores, consulte Montones de [descriptores visibles](shader-visible-descriptor-heaps.md) del sombreador y Montones de [descriptores visibles que](non-shader-visible-descriptor-heaps.md)no son de sombreador.

## <a name="resource-binding-flow-of-control"></a>Flujo de control de enlace de recursos

Al centrarse solo en firmas raíz, descriptores raíz, constantes raíz, tablas de descriptores y montones de descriptores, el flujo de lógica de representación de una aplicación debe ser similar al siguiente:

-   Cree uno o varios objetos de firma raíz: uno para cada configuración de enlace diferente que necesita una aplicación.
-   Cree sombreadores y el estado de canalización con los objetos de firma raíz con los que se usarán.
-   Cree uno (o, si es necesario, más) montones de descriptores que contendrán todos los descriptores SRV, UAV y CBV para cada fotograma de representación.
-   Inicialice los montones de descriptores con descriptores siempre que sea posible para los conjuntos de descriptores que se reutilizarán en muchos fotogramas.
-   Para cada fotograma que se va a representar:
    -   Para cada lista de comandos:
        -   Establezca la firma raíz actual que se va a usar (y cambie si es necesario durante la representación, lo que rara vez es necesario).
        -   Actualice algunas constantes de firma raíz o descriptores de firma raíz para la nueva vista (por ejemplo, proyecciones world/view).
        -   Para cada elemento que se dibujará:
            -   Defina los descriptores nuevos en los montones de descriptores según sea necesario para la representación por objeto. En el caso de los montones de descriptores visibles del sombreador, la aplicación debe asegurarse de usar el espacio del montón de descriptores al que aún no se hace referencia mediante la representación que podría estar en ejecución; por ejemplo, asignar linealmente espacio a través del montón de descriptores durante la representación.
            -   Actualice la firma raíz con punteros a las regiones necesarias de los montones de descriptores. Por ejemplo, una tabla de descriptores podría apuntar a algunos descriptores estáticos (sin intercambiar) inicializados anteriormente, mientras que otra tabla de descriptores podría apuntar a algunos descriptores dinámicos configurados para la representación actual.
            -   Actualice algunas constantes de firma raíz o descriptores de firma raíz para la representación por elemento.
            -   Establezca el estado de canalización del elemento que se va a dibujar (solo si es necesario cambiar), compatible con la firma raíz enlazada actualmente.
            -   Dibujar
        -   Repetir (siguiente elemento)
    -   Repetir (siguiente lista de comandos)
    -   Estrictamente cuando la GPU ha finalizado con cualquier memoria que ya no se usará, se puede liberar. No es necesario eliminar las referencias de descriptores a él si no se envía una representación adicional que use esos descriptores. Por lo tanto, la representación posterior puede apuntar a otras áreas de los montones de descriptores, o los descriptores obsoletos se pueden sobrescribir con descriptores válidos para reutilizar el espacio del montón de descriptores.
-   Repetir (fotograma siguiente)

Tenga en cuenta que otros tipos de descriptores, vistas de destino de representación (RTV), vistas de galería de símbolos de profundidad (DSV), vistas de búfer de índice (IBV), vistas de búfer de vértices (VBV) y vistas de objetos de sombreador (SOV) se administran de forma diferente. El controlador controla el control de versiones del conjunto de descriptores enlazado para cada dibujo durante la grabación de la lista de comandos (de forma similar a la forma en que el hardware o controlador controle las versiones de los enlaces de firma raíz). Esto es diferente del contenido de los montones de descriptores visibles del sombreador, para los que la aplicación debe asignar manualmente a través del montón, ya que hace referencia a descriptores diferentes entre los draws. El control de versiones del contenido del montón que es visible en el sombreador se deja a la aplicación porque permite a las aplicaciones hacer cosas como reutilizar descriptores que no cambian, o usar grandes conjuntos estáticos de descriptores y usar la indexación de sombreador (por ejemplo, por identificador de material) para seleccionar descriptores que se van a usar desde el montón de descriptores, o usar combinaciones de técnicas para diferentes conjuntos de descriptores. El hardware no está equipado para controlar este tipo de flexibilidad para los demás tipos de descriptor (RTV, DSV, IBV, VBV, SOV).

## <a name="suballocation"></a>Suballocation

En Direct3D 12, la aplicación tiene un control de bajo nivel sobre la administración de memoria. En versiones anteriores de Direct3D, incluida Direct3D 11, habría una asignación por recurso. En Direct3D 12, la aplicación puede usar la API para asignar un gran bloque de memoria, mayor de lo que cualquier único objeto necesita. Una vez hecho esto, la aplicación puede crear descriptores que apunten a secciones de ese bloque de memoria grande. Este proceso de decidir qué colocar donde (bloques más pequeños dentro del bloque grande) se conoce como *suballocation*. La habilitación de la aplicación para ello puede producir mejoras en el uso eficaz del cálculo y la memoria. Por ejemplo, el cambio de nombre de los recursos se representa obsoleto. En lugar de esto, las aplicaciones pueden usar barreras para determinar cuándo se usa un recurso determinado y cuándo no mediante barreras en ejecuciones de lista de comandos donde la lista de comandos requiere el uso de ese recurso en particular.

## <a name="freeing-resources"></a>Liberar recursos

Antes de que se pueda liberar cualquier memoria enlazada a la canalización, la GPU debe terminar con ella.

Esperar a la representación de fotogramas es probablemente la manera más general de estar seguro de que la GPU ha finalizado. En un nivel más fino, puede volver a usar barreras: cuando un comando se registra en una lista de comandos de la que desea realizar un seguimiento de la finalización, inserte una barrera inmediatamente después de ella. A continuación, puede realizar varias operaciones de sincronización con la barrera. Envíe un nuevo trabajo (listas de comandos) que espere hasta que haya pasado una barrera especificada en la GPU, lo que indica que todo antes de que se complete, o bien puede solicitar que se cree un evento de CPU cuando se haya superado la barrera (que la aplicación puede estar esperando con un subproceso en modo de espera). En Direct3D 11, esto era `EnqueueSetEvent` ().

## <a name="related-topics"></a>Temas relacionados

* [Enlace de recursos](resource-binding.md)
