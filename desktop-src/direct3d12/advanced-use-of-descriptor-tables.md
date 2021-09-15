---
title: Uso avanzado de tablas descriptores
description: En las secciones siguientes se proporciona información sobre el uso avanzado de tablas de descriptores.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 79dad6914cff07726c2d40ed2ee27cccb6a0cf1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568440"
---
# <a name="advanced-use-of-descriptor-tables"></a>Uso avanzado de tablas descriptores

En las secciones siguientes se proporciona información sobre el uso avanzado de tablas de descriptores.

-   [Cambiar entradas de tabla descriptor entre llamadas de representación](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indexación fuera de límites](#out-of-bounds-indexing)
-   [Derivados del sombreador e indexación divergente](#shader-derivatives-and-divergent-indexing)
-   [Temas relacionados](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Cambiar entradas de tabla descriptor entre llamadas de representación

Después de que las listas de comandos que establecen tablas de descriptores se hayan enviado a una cola para su ejecución, la aplicación no debe editar desde la CPU las partes de los montones de descriptores a los que la GPU podría hacer referencia hasta que la aplicación sepa que la GPU ha terminado de usar las referencias.

La finalización del trabajo se puede determinar en un límite estricto mediante barreras de API para realizar el seguimiento del progreso de la GPU o mecanismos más completos, como esperar a ver que la representación se ha enviado para mostrarse, lo que mejor se adapte a la aplicación. Si una aplicación sabe que solo se accederá a un subconjunto de la región a la que apunta una tabla de descriptores (por ejemplo, debido al control de flujo en el sombreador), los demás descriptores sin referencia todavía pueden cambiarse. Si una aplicación necesita cambiar entre diferentes tablas de descriptores entre las llamadas de representación, hay algunos enfoques entre los que puede elegir la aplicación:

-   Control de versiones de tabla de descriptores: cree (o reutilice) una tabla de descriptores independiente para cada colección única de descriptores a la que haga referencia una lista de comandos. Al editar y volver a usar áreas rellenadas previamente en montones de descriptores, las aplicaciones deben asegurarse primero de que la GPU ha terminado de usar cualquier parte de un montón de descriptores que se reciclará.
-   Indexación dinámica: las aplicaciones pueden organizar objetos que varían según el dibujo o el envío (o incluso variar dentro de un dibujo) en un intervalo de un montón de descriptores, definir una tabla de descriptores que abarque todos ellos y, desde el sombreador, usar la indexación dinámica de la tabla durante la ejecución del sombreador para seleccionar el objeto que se va a usar.
-   Colocación de descriptores en la firma raíz directamente. Solo se puede administrar un número muy pequeño de descriptores de esta manera porque el espacio de firma raíz está limitado.

La implicación de usar el control de versiones de tabla de descriptores es que la memoria de descriptor fuera de un montón de descriptores se debe atravesar para cada conjunto único de descriptores al que hace referencia la canalización de gráficos para cada lista de comandos que se puedan ejecutar, poner en cola para su ejecución o grabarse en un momento dado.

D3D12 deja la responsabilidad de administrar el control de versiones en la aplicación para los tipos de objeto administrados a través de montones de descriptores y tablas de descriptores. Una ventaja de esto es que las aplicaciones pueden optar por reutilizar el contenido de la tabla descriptor tanto como sea posible en lugar de definir siempre una nueva versión de tabla descriptor para cada envío de lista de comandos. La firma raíz es un espacio que el controlador D3D12 versiones automáticamente.

La capacidad de enlazar varias tablas de descriptores a la firma raíz (y, por tanto, a la canalización) a la vez permite a las aplicaciones agrupar y cambiar conjuntos de referencias de descriptor a distintas frecuencias si así lo desean. Por ejemplo, una aplicación podría usar un número pequeño (quizás solo uno) de tablas de descriptores estáticos grandes que rara vez cambian, o en qué regiones de la memoria del montón del descriptor subyacente se rellenan según sea necesario, con el uso de indexación dinámica desde el sombreador para seleccionar texturas. Al mismo tiempo, la aplicación podría mantener otra clase de recursos donde el conjunto al que hace referencia cada llamada a draw se cambia de la CPU mediante la técnica de control de versiones de tabla descriptor.

## <a name="out-of-bounds-indexing"></a>Indexación fuera de límites

La indexación fuera de límites de cualquier tabla de descriptores del sombreador da como resultado un acceso a memoria no definido en gran medida, incluida la posibilidad de leer memoria arbitraria en proceso como si se tratase de un descriptor de estado de hardware y con la consecuencia de lo que hace el hardware con eso. Esto podría producir un restablecimiento del dispositivo, pero no se bloqueará Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Derivados del sombreador e indexación divergente

Si las invocaciones de sombreador de píxeles que se ejecutan en una marca 2x2 (para admitir cálculos derivados) eligen índices de textura diferentes para muestrear desde fuera de una tabla descriptor y si la configuración y textura del muestreador seleccionados para un píxel determinado requiere un cálculo de LOD a partir de derivados de coordenadas de textura, el proceso de muestreo de textura y cálculo de LOD lo realiza el hardware de forma independiente para cada búsqueda de textura en la marca 2x2,  que afectará al rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> </dl>

 

 




