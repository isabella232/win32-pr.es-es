---
description: Los eventos son una parte fundamental del control de llamadas en TAPI 3. El control de eventos incluye cuatro fases.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventos (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545454"
---
# <a name="events-telephony-api"></a>Eventos (API de telefonía)

Los eventos son una parte fundamental del control de llamadas en TAPI 3. El control de eventos incluye cuatro fases.

**Para registrarse y habilitar la recepción de eventos**

1.  Implemente el método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) . (TAPI llama a este método cuando se produce un evento). Normalmente, esta implementación no hace más que **AddRef** el puntero de interfaz **IDispatch** y, a continuación, se envía al bombeo de mensajes de la aplicación.
2.  Registre la interfaz de salida de [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) con las interfaces estándar de com [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) y pase el método [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) a un puntero a [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Llame al método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) para indicar a TAPI los eventos que controlará la aplicación. El filtro de eventos consta de **o** Ed miembros de la enumeración de [**\_ eventos TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > Debe llamar al método **ITTAPI::p UT \_ EventFilter** para establecer la máscara del filtro de eventos y habilitar la recepción de eventos. Si no llama a **ITTAPI::p UT \_ EventFilter**, la aplicación no recibirá ningún evento.

     

También debe llamar al método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) para cada objeto de dirección en el que la aplicación controlará las llamadas.

Vea [interfaces de eventos](./event-interfaces.md) para obtener una lista de todas las interfaces de eventos. Consulte [registrar eventos](register-events.md) para ver ejemplos de código que ilustran el proceso de registro y [recibir una llamada](receive-a-call.md) para obtener un ejemplo de código que muestra un uso de los eventos.

 

 
