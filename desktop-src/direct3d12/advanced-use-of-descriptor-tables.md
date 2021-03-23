---
title: Uso avanzado de las tablas de descriptores
description: En las secciones siguientes se proporciona información sobre el uso avanzado de las tablas de descriptores.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 79dad6914cff07726c2d40ed2ee27cccb6a0cf1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104423"
---
# <a name="advanced-use-of-descriptor-tables"></a>Uso avanzado de las tablas de descriptores

En las secciones siguientes se proporciona información sobre el uso avanzado de las tablas de descriptores.

-   [Cambiar las entradas de la tabla de descriptores entre las llamadas de representación](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indexación fuera de los límites](#out-of-bounds-indexing)
-   [Derivados del sombreador e indexación divergente](#shader-derivatives-and-divergent-indexing)
-   [Temas relacionados](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Cambiar las entradas de la tabla de descriptores entre las llamadas de representación

Una vez que el comando muestra una lista de las tablas de descriptores establecidas en una cola para su ejecución, la aplicación no debe editar desde la CPU las partes de los montones descriptores a los que puede hacer referencia la GPU hasta que la aplicación sepa que la GPU ha terminado de usar las referencias.

La finalización del trabajo se puede determinar en un estrecho límite mediante las barreras de API para realizar un seguimiento del progreso de la GPU, o mecanismos más generales como esperar para ver que se ha enviado la representación a la pantalla, lo que se adapte a la aplicación. Si una aplicación sabe que solo se tendrá acceso a un subconjunto de la región a la que apunta una tabla de descriptores (por ejemplo, debido al control de flujo en el sombreador), los otros descriptores sin referencia todavía se pueden cambiar. Si una aplicación necesita cambiar entre diferentes tablas de descriptores entre las llamadas de representación, existen varios enfoques entre los que la aplicación puede elegir:

-   Control de versiones de tabla de descriptor: crear (o reutilizar) una tabla de descriptores independiente para cada colección de descriptores única a la que se va a hacer referencia mediante una lista de comandos. Al editar y volver a usar áreas previamente rellenadas en montones de descriptores, las aplicaciones deben asegurarse primero de que la GPU ha terminado de usar cualquier parte de un montón de descriptores que se recicle.
-   Indexación dinámica: las aplicaciones pueden organizar objetos que varíen en Draw/dispatch (o incluso variar dentro de un dibujo) en un intervalo de un montón de descriptores, definir una tabla de descriptores que abarque todos ellos y, desde el sombreador, usar la indexación dinámica de la tabla durante la ejecución del sombreador para seleccionar el objeto que se va a usar.
-   Colocar los descriptores en la firma raíz directamente. Solo se puede administrar un número muy pequeño de descriptores de esta manera, ya que el espacio de la firma raíz es limitado.

La implicación de usar el control de versiones de la tabla de descriptores es que la memoria de descriptor de un montón de descriptores debe grabarse a través de cada conjunto de descriptores único al que se hace referencia en la canalización de gráficos para cada lista de comandos que se puede ejecutar, poner en cola para su ejecución o grabarse en un momento dado.

D3D12 deja la responsabilidad de administrar el control de versiones en la aplicación para los tipos de objeto administrados mediante montones de descriptor y tablas de descriptores. Una ventaja de esto es que las aplicaciones pueden optar por reutilizar el contenido de la tabla de descriptores lo máximo posible en lugar de definir siempre una nueva versión de la tabla de descriptores para cada envío de la lista de comandos. La firma raíz es un espacio que el controlador D3D12 de forma automática.

La capacidad de enlazar varias tablas de descriptores a la firma raíz (y, por tanto, a la canalización) a la vez permite a las aplicaciones agrupar y cambiar conjuntos de referencias de descriptores en diferentes frecuencias si se desea. Por ejemplo, una aplicación podría usar un número pequeño (quizás solo uno) de grandes tablas de descriptores estáticos que rara vez cambian, o en qué regiones de la memoria del montón del descriptor subyacente se están llenando según sea necesario, con el uso de la indexación dinámica del sombreador para seleccionar las texturas. Al mismo tiempo, la aplicación podría mantener otra clase de recursos en los que el conjunto al que hace referencia cada llamada a Draw se cambie de la CPU mediante la técnica de control de versiones de la tabla de descriptores.

## <a name="out-of-bounds-indexing"></a>Indexación fuera de los límites

Fuera de los límites, la indización de cualquier tabla de descriptores del sombreador da como resultado un acceso a memoria en gran medida, lo que incluye la posibilidad de leer la memoria en proceso arbitraria como si fuera un descriptor de estado de hardware y vivir con la consecuencia de lo que hace el hardware. Esto podría producir un restablecimiento del dispositivo, pero no bloqueará Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Derivados del sombreador e indexación divergente

Si las invocaciones del sombreador de píxeles que se ejecutan en una marca de 2x2 (para admitir cálculos derivados) eligen índices de textura diferentes para muestrear de una tabla de descriptores, además, si la configuración de muestra seleccionada y la textura de un píxel determinado requieren un cálculo de LOD de derivados de coordenadas de textura, el hardware se realiza de forma independiente por cada búsqueda de textura en la marca de 2x2. , que afectará al rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> </dl>

 

 




