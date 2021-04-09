---
title: Contexto (servicios Web de Windows)
description: Se usa un contexto en las operaciones de servicio de modelo de servicio y las devoluciones de llamada para pasar datos de estado pertinentes a la operación de servicio o devolución de llamada cuando se invoca.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Servicios Web de contexto para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103994847"
---
# <a name="context-windows-web-services"></a>Contexto (servicios Web de Windows)

Se usa un contexto en [las operaciones](service-operation.md) de servicio de modelo de servicio y las devoluciones de llamada para pasar datos de estado pertinentes a la operación de servicio o devolución de llamada cuando se invoca. Una estructura de [ \_ \_ contexto de operación WS](ws-operation-context.md) hace referencia a un contexto. Las propiedades de un contexto se pueden recuperar con la función [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , como se muestra en el código siguiente.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

No todas las propiedades de contexto están disponibles en un momento dado. Vea la documentación de la propiedad de contexto relativa a la disponibilidad de una propiedad específica en una devolución de llamada o una [operación de servicio](service-operation.md).

Para obtener más información sobre cómo mantener la duración y el subprocesamiento de los contextos de la operación, vea el tema [duración del contexto de operación y subprocesamiento](operation-context-lifetime-and-threading.md) .

La enumeración siguiente forma parte del contexto:

-   [**identificador de la propiedad de contexto de \_ operación WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

La siguiente función forma parte del contexto:

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

El siguiente identificador forma parte del contexto:

-   [\_contexto de operación WS \_](ws-operation-context.md)

 

 




