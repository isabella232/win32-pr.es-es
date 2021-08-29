---
description: Para publicar un evento, simplemente cree una instancia de un objeto de clase de evento e invoque el método deseado. Para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea Publicación de un evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publicación y entrega de eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de1625d1e18340d71b3ad3a53c06d2db79b9fd1f913e7a49274644bc3a715c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812866"
---
# <a name="publishing-and-delivering-events-in-com"></a>Publicación y entrega de eventos en COM+

Para publicar un evento, simplemente cree una instancia de un objeto [de clase de](the-com--event-class-object.md) evento e invoque el método deseado. Para obtener instrucciones detalladas sobre cómo hacerlo en el código, vea [Publicación de un evento](publishing-an-event.md).

Cuando un publicador activa un evento, el servicio eventos COM+ busca en la base de datos de suscripciones todos los suscriptores que han registrado suscripciones a la clase de eventos con instancias. Se conecta a esos suscriptores (mediante creación directa, monikers o componentes en cola) y llama al método . Para admitir más de una notificación de suscriptor para un evento, los métodos solo pueden contener en parámetros y solo deben devolver valores **HRESULT** correctos o de error.

> [!Note]  
> Esta versión de eventos COM+ no admite un almacén de eventos distribuido. Un suscriptor debe suscribirse a un evento en cada equipo desde el que desea recibir la notificación. Como alternativa, puede registrar el objeto de clase de eventos y las suscripciones en un equipo central y crear instancias de este objeto de clase de eventos desde los equipos remotos en los que publica eventos. DCOM o el servicio de componentes en cola de COM+ proporcionan la entrega de eventos. Para obtener más información sobre el uso del servicio de componentes en cola de COM+, vea [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).

 

De forma predeterminada, el servicio de eventos COM+ activa eventos de uno en uno, sin ningún orden determinado o repetible. Los publicadores que necesitan controlar el orden en el que los suscriptores reciben un evento pueden implementar un filtro de publicador. (Para obtener más información, vea [Filtrado de eventos en COM+).](filtering-events-in-com-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[El objeto de clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso de eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



