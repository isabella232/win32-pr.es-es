---
title: Eventos
description: Un servicio hospedado debe implementar la interfaz IUPnPEventSource si tiene variables de estado con eventos.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a6382ee88d2ca5168c94eac20727bbfee4a598
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903537"
---
# <a name="eventing"></a>Eventos

Un servicio hospedado debe implementar la interfaz [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) si tiene variables de estado con eventos. Esta interfaz tiene dos métodos: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) y [**unaconseje**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Esta interfaz proporciona un mecanismo para que el host del dispositivo se suscriba a las notificaciones de eventos generadas por el servicio hospedado. No habrá más de un receptor de eventos registrado a la vez.

Un servicio hospedado debe implementar el método [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) manteniendo una referencia a la interfaz [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) , que se pasó como parámetro. Si se encuentra la interfaz, el método **Advise** contiene una referencia a esa interfaz hasta que se invoca [**unaconsejable**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) , o hasta que se quita el objeto de servicio hospedado. Solo se llama una vez a **Advise** .

Para quitar la suscripción, el host del dispositivo invoca [**unvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) y pasa el puntero del objeto usado cuando llamó a [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). El servicio hospedado quita la suscripción si el puntero es el mismo que el que se pasa a **Advise**.

Cuando cambia el valor de una variable de estado, el servicio hospedado debe indicar que se ha producido un evento. Para ello, los servicios invocan el método [**IUPnPEventSink:: OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) .

Cuando el host del dispositivo ya no necesita recibir notificaciones del servicio hospedado, invoca [**IUPnPEventSource:: unvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), pasando el mismo puntero de objeto que recibió de [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). El host del dispositivo invoca este método cuando el dispositivo ya no va a estar en la red.

 

 




