---
description: Acerca del Administrador de Graph filtros
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: Acerca del Administrador de Graph filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162453"
---
# <a name="about-the-filter-graph-manager"></a>Acerca del Administrador de Graph filtros

Filter [Graph Manager es](filter-graph-manager.md) un objeto COM que controla los filtros de un gráfico de filtros. Realiza muchas funciones, incluidas las siguientes:

-   Coordinación de los cambios de estado entre los filtros.
-   Establecer un reloj de referencia.
-   Comunicar eventos de vuelta a la aplicación.
-   Proporcionar métodos para que las aplicaciones compilen el gráfico de filtros.

Cada una de estas funciones se describe brevemente aquí. Los detalles se pueden encontrar en otra parte de la documentación.

**Cambios de estado.** Los cambios de estado dentro de los filtros deben producirse en un orden determinado. Por lo tanto, la aplicación no emite comandos de cambio de estado directamente a los filtros. En su lugar, proporciona un único comando al Administrador de Graph, que distribuye el comando a cada uno de los filtros. La búsqueda funciona de forma similar: la aplicación proporciona un comando seek al Administrador de filtros Graph, que lo distribuye a los filtros.

**Reloj de referencia.** Todos los filtros del gráfico usan el mismo reloj, denominado reloj *de referencia*. El reloj de referencia garantiza que todas las secuencias estén sincronizadas. La hora a la que se debe representar un fotograma de vídeo o una muestra de audio se denomina tiempo *de presentación.* El tiempo de presentación se mide con respecto al reloj de referencia. El Administrador Graph filtros elige un reloj de referencia, normalmente el reloj de la tarjeta de sonido o el reloj del sistema.

**Graph eventos**. Filter Graph Manager usa una cola de eventos para informar a la aplicación de los eventos que se producen en el gráfico de filtros. Este mecanismo es similar a un bucle Windows mensaje.

**Graph métodos de creación de archivos**. Filter Graph Manager proporciona métodos para que la aplicación agregue filtros al gráfico, conecte filtros a otros filtros y desconecte los filtros.

Una función que el Administrador de Graph no controla es mover datos de un filtro al siguiente. Esto lo hacen los propios filtros, a través de sus conexiones de pin. El procesamiento siempre se produce en un subproceso independiente.

> [!Note]  
> Los filtros siempre son de subproceso libre, residen en el mismo proceso que el Administrador de Graph y se cargan desde servidores en proceso. Por lo tanto, las llamadas al método no se serializan entre filtros ni entre filtros y el Administrador de Graph filtros.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Establecimiento del Graph reloj](setting-the-graph-clock.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



