---
description: Los eventos son una parte fundamental del control de llamadas en TAPI 3. El control de eventos incluye cuatro fases.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventos (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b2cf181f10373505a0fe50d3c9efa7358b3ccb749acb723d8314dee27ff9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660865"
---
# <a name="events-telephony-api"></a>Eventos (API de telefonía)

Los eventos son una parte fundamental del control de llamadas en TAPI 3. El control de eventos incluye cuatro fases.

**Para registrarse y habilitar la recepción de eventos**

1.  Implemente [**el método ITTAPIEventNotification::Event.**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) (TAPI llama a este método cuando se produce un evento). Normalmente, esta implementación no hace más que **AddRef** el puntero de interfaz **IDispatch** y, a continuación, publica en el bombeo de mensajes de la aplicación.
2.  Registre la interfaz saliente [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) mediante las interfaces estándar COM [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) y pase al método [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un puntero a [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Llame al [**método \_ EVENTFilter ITTAPI::p ut**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) para decir a TAPI qué eventos controlará la aplicación. El filtro de eventos consta de **miembros or** ed de la [**enumeración TAPI \_ EVENT.**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
    > [!Note]  
    > Debe llamar al método **ITTAPI::p ut \_ EventFilter** para establecer la máscara de filtro de eventos y habilitar la recepción de eventos. Si no llama a **ITTAPI::p ut \_ EventFilter**, la aplicación no recibirá ningún evento.

     

También debe llamar al método [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) para cada objeto de dirección en el que la aplicación controlará las llamadas.

Consulte [Interfaces de eventos](./event-interfaces.md) para obtener una lista de todas las interfaces de eventos. Vea [Registrar eventos para](register-events.md) obtener ejemplos de código que ilustran el proceso de registro y [Recibir](receive-a-call.md) una llamada para un ejemplo de código que muestra un uso de eventos.

 

 
