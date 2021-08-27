---
title: Contexto (Windows Web Services)
description: Se usa un contexto en las operaciones de servicio del modelo de servicio y las devoluciones de llamada para pasar los datos de estado pertinentes a la operación o devolución de llamada del servicio cuando se invocan.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Servicios web de contexto para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026633"
---
# <a name="context-windows-web-services"></a>Contexto (Windows Web Services)

Se usa un contexto [](service-operation.md) en las operaciones de servicio del modelo de servicio y las devoluciones de llamada para pasar los datos de estado pertinentes a la operación o devolución de llamada del servicio cuando se invocan. Una estructura CONTEXT de WS OPERATION hace referencia a [ \_ \_ un](ws-operation-context.md) contexto. Las propiedades de un contexto se pueden recuperar con la función [**WsGetOperationContextProperty,**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) como se muestra en el código siguiente.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

No todas las propiedades de contexto están disponibles en un momento dado. Consulte la documentación de la propiedad de contexto relativa a la disponibilidad de una propiedad específica en una devolución de llamada o una [operación de servicio](service-operation.md).

Para obtener más información sobre cómo mantener la duración del contexto de operación y el subprocesamiento, vea el tema [Duración](operation-context-lifetime-and-threading.md) del contexto de operación y subprocesamiento.

La enumeración siguiente forma parte del contexto:

-   [**IDENTIFICADOR DE PROPIEDAD \_ DEL CONTEXTO DE OPERACIÓN \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

La siguiente función forma parte del contexto:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

El siguiente identificador forma parte del contexto:

-   [CONTEXTO DE OPERACIÓN DE WS \_ \_](ws-operation-context.md)

 

 




