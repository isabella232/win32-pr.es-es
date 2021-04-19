---
description: Acerca del administrador de gráficos de filtros
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Acerca del administrador de gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537833"
---
# <a name="about-the-filter-graph-manager"></a>Acerca del administrador de gráficos de filtros

[Filter Graph Manager](filter-graph-manager.md) es un objeto com que controla los filtros de un gráfico de filtro. Realiza muchas funciones, entre las que se incluyen las siguientes:

-   Coordinación de los cambios de estado entre los filtros.
-   Establecer un reloj de referencia.
-   Comunicar los eventos de nuevo a la aplicación.
-   Proporcionar métodos para que las aplicaciones generen el gráfico de filtro.

Cada una de estas funciones se describe brevemente aquí. Los detalles se pueden encontrar en cualquier parte de la documentación.

**Cambios de estado**. Los cambios de estado dentro de los filtros deben aparecer en un orden determinado. Por lo tanto, la aplicación no emite comandos de cambio de estado directamente a los filtros. En su lugar, proporciona un solo comando al administrador de gráficos de filtro, que distribuye el comando a cada uno de los filtros. La búsqueda funciona de manera similar: la aplicación proporciona un comando de búsqueda al administrador de gráficos de filtro, que lo distribuye a los filtros.

**Reloj de referencia**. Todos los filtros del gráfico usan el mismo reloj, denominado *reloj de referencia*. El reloj de referencia garantiza que todos los flujos están sincronizados. La hora a la que se debe representar un fotograma de vídeo o un ejemplo de audio se denomina *tiempo de presentación*. El tiempo de presentación se mide en relación con el reloj de referencia. El administrador de gráficos de filtro elige un reloj de referencia, normalmente el reloj de la tarjeta de sonido o el reloj del sistema.

**Eventos de gráfico**. Filter Graph Manager usa una cola de eventos para informar a la aplicación de los eventos que se producen en el gráfico de filtro. Este mecanismo es similar a un bucle de mensajes de Windows.

**Métodos de creación de gráficos**. Filter Graph Manager proporciona métodos para que la aplicación agregue filtros al gráfico, conecte filtros a otros filtros y desconecte filtros.

Una función que el administrador de gráficos de filtro no controla es mover los datos de un filtro al siguiente. Esto se realiza mediante los propios filtros, a través de sus conexiones de PIN. El procesamiento se produce siempre en un subproceso independiente.

> [!Note]  
> Los filtros siempre son de subproceso libre, residen en el mismo proceso que el administrador de gráficos de filtro y se cargan desde servidores en proceso. Por lo tanto, no se calculan las referencias de las llamadas a métodos entre los filtros o entre los filtros y el administrador de gráficos de filtro.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Establecer el reloj del gráfico](setting-the-graph-clock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



