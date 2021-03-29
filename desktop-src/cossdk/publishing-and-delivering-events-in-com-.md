---
description: Para publicar un evento, simplemente cree una instancia de un objeto de clase de evento e invoque el método deseado; para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea publicar un evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publicar y entregar eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807790"
---
# <a name="publishing-and-delivering-events-in-com"></a>Publicar y entregar eventos en COM+

Para publicar un evento, simplemente cree una instancia de un objeto de [clase de evento](the-com--event-class-object.md) e invoque el método deseado; para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea [publicar un evento](publishing-an-event.md).

Cuando un publicador desencadena un evento, el servicio de eventos COM+ busca en la base de datos de suscripciones para encontrar todos los suscriptores que han registrado suscripciones a la clase de eventos con instancias. Se conecta a los suscriptores (mediante la creación directa, monikers o componentes en cola) y llama al método. Para admitir más de una notificación de suscriptor para un evento, los métodos solo pueden contener parámetros in y deben devolver valores **HRESULT** correctos o con errores.

> [!Note]  
> Esta versión de eventos COM+ no es compatible con un almacén de eventos distribuido. Un suscriptor debe suscribirse a un evento en cada equipo desde el que desea recibir la notificación. Como alternativa, puede registrar el objeto de la clase de evento y las suscripciones en un equipo central y crear una instancia de este objeto de la clase de evento desde los equipos remotos en los que se publican los eventos. La entrega de eventos se proporciona mediante DCOM o el servicio de componentes en cola de COM+. Para obtener más información acerca del uso del servicio de componentes en cola de COM+, vea [using com+ events with com+ queued Components](using-com--events-with-com--queued-components.md).

 

De forma predeterminada, el servicio de eventos COM+ activa los eventos de uno en uno, sin ningún orden determinado o repetible. Los publicadores que necesiten controlar el orden en el que los suscriptores reciben un evento pueden implementar un filtro de publicador. (Para obtener más información, vea [filtrar eventos en com+](filtering-events-in-com-.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[Objeto de la clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Usar eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



