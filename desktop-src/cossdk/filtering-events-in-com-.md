---
description: 'Los eventos COM+ ofrecen dos maneras de controlar qué eventos llegan a los suscriptores: filtrado de publicador y filtrado de parámetros.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrado de eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807796"
---
# <a name="filtering-events-in-com"></a>Filtrado de eventos en COM+

Los eventos COM+ ofrecen dos maneras de controlar qué eventos llegan a los suscriptores: *filtrado de publicador* y *filtrado de parámetros*.

## <a name="publisher-filtering"></a>Filtrado de publicador

El filtrado de publicador controla el orden y la activación de un método de evento mediante un objeto de [clase de evento](the-com--event-class-object.md) . El filtrado de publicadores permite al publicador determinar qué suscriptores reciben un evento determinado.

Un ejemplo de uso eficaz del filtrado de publicador es el de una bolsa de valores. La mayoría de los suscriptores quieren saber cuándo se agrega una nueva cotización. Sin embargo, es posible que muchos de estos suscriptores no deseen saber cada vez que cambien los precios de las acciones. El filtrado de publicador proporciona la granularidad necesaria para ofrecer eficazmente eventos a solo los suscriptores que desean esta información.

Cuando se invoca un método en el objeto de clase de eventos con instancias, se recopilan los filtros de publicador en ese método. El filtro fuerza el objeto de evento a desencadenar el método de evento para un suscriptor concreto. El filtro determina qué suscripciones se activarán y en qué orden se activarán. Por ejemplo, el filtro podría leer la lista de suscripciones y crear el pedido basándose en algunos criterios de aplicación y, a continuación, llamar a los suscriptores en ese orden.

Para obtener instrucciones detalladas sobre cómo crear un filtro de publicador, consulte [crear un filtro de publicador](creating-a-publisher-filter.md).

## <a name="parameter-filtering"></a>Filtro de parámetros

A diferencia del filtrado de publicador, el servicio de eventos COM+ proporciona un filtrado de parámetros de suscriptor opcional para cada suscripción y cada invocación de método de evento. El filtrado de parámetros evalúa la propiedad FilterCriteria de la suscripción con los parámetros del método de evento. Este tipo de filtrado se utiliza por cada método y suscripción, y proporciona un nivel de filtrado de suscriptores en el origen del evento. La cadena de criterios de filtro reconoce los operadores relacionales para comprobar la igualdad (=, = =,!,! =, ~, ~ =,  <>), los paréntesis anidados y las palabras clave lógicas **and**, **or** o **Not**.

El filtrado de parámetros se produce después de cualquier filtro de publicador y cuando se desencadena el objeto de evento estándar para una suscripción determinada. Si se usa el filtrado del publicador, el filtrado de parámetros solo se produce cuando el filtro del publicador invoca [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription). Por este motivo, el filtrado de publicadores y el filtrado de parámetros pueden componerse juntos, pero el filtrado del publicador tiene prioridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[Objeto de la clase de eventos COM+](the-com--event-class-object.md)
</dt> <dt>

[Usar eventos COM+ con componentes en cola de COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



