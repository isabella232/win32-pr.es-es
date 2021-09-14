---
description: Lavado
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Lavado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575f311020c2c7a567e544b80ba323a29051cc38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063270"
---
# <a name="flushing"></a>Lavado

Mientras se ejecuta el gráfico de filtros, se pueden mover cantidades arbitrarias de datos a través del gráfico. Algunas de estas pueden estar en colas, a la espera de ser entregadas. Hay ocasiones en las que el gráfico de filtros necesita quitar estos datos pendientes lo antes posible y reemplazarlos por nuevos datos. Después de un comando seek, por ejemplo, el filtro de origen genera ejemplos a partir de una nueva posición en el origen. Para minimizar la latencia, los filtros de nivel inferior deben descartar las muestras que se crearon antes del comando seek. El proceso de descartar muestras se denomina *vaciado.* Permite que el gráfico tenga más capacidad de respuesta cuando los eventos modifican el flujo de datos normal.

El vaciado se controla de forma ligeramente diferente en el modelo de extracción que el modelo de inserción. Este artículo comienza por describir el modelo de inserción; a continuación, describe las diferencias en el modelo de extracción.

El vaciado se produce en dos fases.

-   En primer lugar, el filtro de origen [**llama a IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el pin de entrada del filtro de bajada. El filtro de nivel inferior comienza a rechazar muestras de nivel superior. También descarta las muestras que está manteniendo y envía la llamada **BeginFlush** de bajada al filtro siguiente.
-   Cuando el filtro de origen está listo para enviar nuevos datos, llama a [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el pin de entrada. Esto indica al filtro de bajada que puede recibir nuevos ejemplos. El filtro de bajada envía **la llamada EndFlush** al filtro siguiente.

En el **método BeginFlush,** el pin de entrada hace lo siguiente:

1.  Llama **a BeginFlush en** los pines de entrada de bajada.
2.  Rechaza cualquier otra llamada que transmita datos, **incluidos Receive** y **EndOfStream.**
3.  Desbloquea los filtros ascendentes que están bloqueados a la espera de una muestra del asignador del filtro. Algunos filtros desasignan sus asignadores para este propósito.
4.  Sale de las esperas que bloquean el streaming. Por ejemplo, los filtros de representador se bloquean cuando se pausan. También se bloquean cuando están esperando para representar un ejemplo en el tiempo de secuencia correcto. El filtro debe desbloquearse para que se puedan entregar y rechazar muestras en cola ascendentes. Este paso garantiza que todos los filtros ascendentes se desbloqueen finalmente.

En el **método EndFlush,** el pin de entrada hace lo siguiente:

1.  Espera a que se descarten todos los ejemplos en cola.
2.  Libera los datos almacenados en búfer. A veces, este paso se puede realizar en **el método BeginFlush.** Sin embargo, **BeginFlush** no está sincronizado con el subproceso de streaming. El filtro no debe procesar ni almacenar en búfer más datos entre la llamada a **BeginFlush** y la llamada a **EndFlush.**
3.  Borra las notificaciones EC \_ COMPLETE pendientes.
4.  Llama **a EndFlush de** bajada.

En este momento, el filtro puede volver a aceptar ejemplos. Se garantiza que todos los ejemplos son más recientes que el vaciado.

En el modelo de extracción, el filtro del analizador inicia el vaciado, en lugar del filtro de origen. No solo llama a  **IPin::BeginFlush** e **IPin::EndFlush** en el filtro de nivel inferior, sino que también llama a [**IAsyncReader::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) e [**IAsyncReader::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) en el pin de salida del filtro de origen. Si el filtro de origen tiene solicitudes de lectura pendientes, las descartará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vaciar datos](flushing-data.md)
</dt> </dl>

 

 



