---
description: 'Eventos COM+ proporciona dos maneras de controlar qué eventos llegan a los suscriptores: filtrado del publicador y filtrado de parámetros.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrado de eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358898"
---
# <a name="filtering-events-in-com"></a>Filtrado de eventos en COM+

Eventos COM+ proporciona dos maneras de controlar qué eventos llegan a los suscriptores: filtrado *del publicador* *y filtrado de parámetros.*

## <a name="publisher-filtering"></a>Publisher Filtrado

Publisher de eventos controla el orden y la activación de un método de evento mediante un [objeto de clase de](the-com--event-class-object.md) evento. Publisher filtrado permite al publicador determinar qué suscriptores reciben un evento determinado.

Un ejemplo de uso efectivo del filtrado del publicador es el de una bolsa de valores. La mayoría de los suscriptores quieren saber cuándo se agrega una nueva acción. Sin embargo, es posible que muchos de estos mismos suscriptores no quieran saber cada vez que cambia el precio de cada acción. Publisher filtrado proporciona la granularidad necesaria para entregar eventos de forma eficaz solo a los suscriptores que desean esta información.

Cuando se invoca un método en el objeto de clase de eventos con instancias, recopila los filtros del publicador en ese método. El filtro fuerza al objeto de evento a que desen marcha el método de evento a un suscriptor específico. El filtro determina qué suscripciones se activan y en qué orden se activan. Por ejemplo, el filtro podría leer la lista de suscripciones y crear el pedido en función de algunos criterios de aplicación y, a continuación, llamar a los suscriptores en ese orden.

Para obtener instrucciones detalladas sobre cómo crear un filtro de publicador, vea [Creating a Publisher Filter](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Filtro de parámetros

A diferencia del filtrado del publicador, el servicio eventos COM+ proporciona un filtrado de parámetros de suscriptor opcional para cada suscripción y cada invocación de método de evento. El filtrado de parámetros evalúa la propiedad FilterCriteria de suscripción con los parámetros del método de evento. Este tipo de filtrado se usa por método y suscripción y proporciona un nivel de filtrado de suscriptor en el origen del evento. La cadena de criterios de filtro reconoce operadores relacionales para comprobar la igualdad (=, ==, !, !=, ~, ~=, <>), paréntesis anidados y palabras clave lógicas **AND**, **OR** o **NOT**.

El filtrado de parámetros se produce después de cualquier filtrado del publicador y cuando se desencadena el objeto de evento estándar para una suscripción determinada. Si se usa el filtrado del publicador, el filtrado de parámetros solo se produce cuando el filtro del publicador invoca [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription). Por este motivo, el filtrado del publicador y el filtrado de parámetros pueden crearse juntos, pero el filtrado del publicador tiene prioridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Publicación y entrega de eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[El objeto de clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Uso de eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



