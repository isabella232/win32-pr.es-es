---
description: El servicio de eventos COM+ se utiliza para administrar la entrega de eventos de publicadores a suscriptores.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Usar eventos COM+ con componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714883"
---
# <a name="using-com-events-with-com-queued-components"></a>Usar eventos COM+ con componentes en cola de COM+

El servicio de eventos COM+ se utiliza para administrar la entrega de eventos de publicadores a suscriptores. El servicio de componentes en cola de COM+ se puede usar para hacer que el publicador y el tiempo de procesamiento del suscriptor sean independientes al poner en cola el mensaje del publicador y, posteriormente, reproducirlo en el suscriptor. Tanto si necesita usar el servicio de componentes en cola depende de la lógica de negocios subyacente de la aplicación. Si necesita tener eventos independientes del tiempo, puede crearlos mediante el servicio de eventos COM+ con el servicio de componentes en cola de COM+.

> [!Note]  
> Para obtener información adicional acerca del uso del servicio de componentes en cola de COM+, vea [componentes en cola de com+](com--queued-components.md).

 

El servicio de componentes en cola mantiene la invocación de orden de método dentro de un solo mensaje. La grabadora procesa por lotes todas las invocaciones de método en un mensaje y, a continuación, el reproductor invoca esos métodos en orden cuando se procesa el mensaje.

Una grabadora de componentes en cola y un reproductor se pueden colocar en cualquiera de los dos lugares siguientes:

-   Entre el publicador y el objeto de evento
-   Entre el objeto de evento y el suscriptor

Si coloca la grabadora y el reproductor entre el publicador y el objeto de evento, hará que el componente de [clase de evento](the-com--event-class-object.md) queuable. El componente de la clase de evento debe marcarse para la puesta en cola y ser activado por el reproductor en un proceso independiente del publicador.

Para proporcionar eventos de forma asincrónica, cree la grabadora y el reproductor entre el objeto de evento y el suscriptor, y establezca el atributo en cola del objeto de suscripción. Esto establece SubscriberMoniker como se indica a continuación: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".

Hay un orden de implicación de entrega que se debe tener en cuenta al usar componentes en cola en una situación de evento. Dado que el servicio de componentes en cola registra y reproduce todas las llamadas dentro de la duración de un solo objeto en un mensaje, todas las llamadas se reproducen en el orden en que se realizaron. Sin embargo, si hay más de una sesión con más de un objeto, no se puede garantizar el orden. Si el orden es importante, asegúrese de que las llamadas que se deben reproducir en orden residan en la misma instancia de objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Suscripciones](subscriptions.md)
</dt> <dt>

[Objeto de la clase de eventos COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



