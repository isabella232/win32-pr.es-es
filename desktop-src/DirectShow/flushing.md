---
description: Vaciar
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Vaciar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575f311020c2c7a567e544b80ba323a29051cc38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537953"
---
# <a name="flushing"></a>Vaciar

Mientras se ejecuta el gráfico de filtros, se pueden mover cantidades arbitrarias de datos a través del gráfico. Algunos de ellos pueden estar en colas, en espera de ser entregados. Hay ocasiones en las que el gráfico de filtros debe quitar estos datos pendientes lo más rápidamente posible y reemplazarlos por datos nuevos. Después de un comando de búsqueda, por ejemplo, el filtro de origen genera ejemplos a partir de una nueva posición en el origen. Para minimizar la latencia, los filtros de nivel inferior deben descartar las muestras que se crearon antes del comando de búsqueda. El proceso de descartar ejemplos se denomina *vaciado*. Permite que el gráfico tenga mayor capacidad de respuesta cuando los eventos modifican el flujo de datos normal.

El modelo de extracción controla de forma ligeramente diferente el vaciado que el modelo de inserción. En este artículo se empieza por describir el modelo de envío. a continuación, se describen las diferencias en el modelo de extracción.

El vaciado se produce en dos fases.

-   En primer lugar, el filtro de origen llama a [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada del filtro de nivel inferior. El filtro de nivel inferior comienza a rechazar ejemplos de nivel superior. También descarta cualquier ejemplo que contiene y envía la llamada **BeginFlush** de nivel inferior al filtro siguiente.
-   Cuando el filtro de origen está listo para enviar datos nuevos, llama a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada. Esto indica al filtro de bajada que puede recibir muestras nuevas. El filtro de nivel inferior envía la llamada **EndFlush** al siguiente filtro.

En el método **BeginFlush** , el PIN de entrada hace lo siguiente:

1.  Llama a **BeginFlush** en clavijas de entrada de nivel inferior.
2.  Rechaza las llamadas posteriores que transmiten los datos, incluidos **Receive** y **EndOfStream**.
3.  Desbloquea todos los filtros ascendentes que están bloqueados en espera de una muestra del asignador del filtro. Algunos filtros anulan la confirmación de los asignadores para este fin.
4.  Sale de cualquier espera que bloquee el flujo. Por ejemplo, los filtros de representador se bloquean cuando están en pausa. También se bloquean cuando están a la espera de representar una muestra en el momento de la secuencia correcta. El filtro debe desbloquearse, de modo que se puedan entregar y rechazar los ejemplos en cola de nivel superior. Este paso garantiza que todos los filtros ascendentes se desbloqueen.

En el método **EndFlush** , el PIN de entrada hace lo siguiente:

1.  Espera a que se descarten todas las muestras en cola.
2.  Libera los datos almacenados en búfer. En ocasiones, este paso se puede realizar en el método **BeginFlush** . Sin embargo, **BeginFlush** no está sincronizado con el subproceso de streaming. El filtro no debe procesar ni almacenar en búfer más datos entre la llamada a **BeginFlush** y la llamada a **EndFlush**.
3.  Borra todas las \_ notificaciones completas de EC pendientes.
4.  Llama a **EndFlush** downstream.

En este momento, el filtro puede aceptar los ejemplos de nuevo. Se garantiza que todos los ejemplos son más recientes que el vaciado.

En el modelo de extracción, el filtro del analizador inicia el vaciado, en lugar del filtro de origen. No solo llama a **IPin:: BeginFlush** y **IPin:: EndFlush** en el filtro de nivel inferior, sino que también llama a [**IAsyncReader:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) y [**IAsyncReader:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) en el PIN de *salida* del filtro de origen. Si el filtro de origen tiene solicitudes de lectura pendientes, se descartarán.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vaciar datos](flushing-data.md)
</dt> </dl>

 

 



