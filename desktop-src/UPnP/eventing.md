---
title: Eventos
description: Un servicio hospedado debe implementar la interfaz IUPnPEventSource si tiene variables de estado de evento.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008085"
---
# <a name="eventing"></a>Eventos

Un servicio hospedado debe implementar la [**interfaz IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) si tiene variables de estado de evento. Esta interfaz tiene dos métodos: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) y [**Unadvise.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) Esta interfaz proporciona un mecanismo para que el host del dispositivo se suscriba a las notificaciones de eventos generadas por el servicio hospedado. No habrá más de un receptor de eventos registrado a la vez.

Un servicio hospedado debe implementar el método [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) manteniendo una referencia a la interfaz [**IUPnPEventSink,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) que se pasó como parámetro. Si se encuentra la interfaz, el método **Advise** contiene una referencia a esa interfaz hasta que se invoca [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) o hasta que se quita el objeto de servicio hospedado. **Se llama** a Advise solo una vez.

Para quitar la suscripción, el host de dispositivo invoca [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) y pasa el puntero de objeto utilizado cuando llamó [**a Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). El servicio hospedado quita la suscripción si el puntero es el mismo que el pasado a **Advise**.

Cuando cambia el valor de una variable de estado, el servicio hospedado debe indicar que se ha producido un evento. Para ello, los servicios invocan el [**método IUPnPEventSink::OnStateChanged.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged)

Cuando el host de dispositivo ya no necesita recibir notificaciones del servicio hospedado, invoca [**a IUPnPEventSource::Unadvise,**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise)pasando el mismo puntero de objeto que recibió de [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). El host de dispositivo invoca este método cuando el dispositivo ya no va a estar en la red.

 

 




