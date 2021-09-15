---
title: Estado de usuario del host de servicio
description: El host de servicio permite que una aplicación asocie datos de estado con ámbito en el nivel de host de servicio.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Servicios web de estado de host de usuario para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360178"
---
# <a name="service-host-user-state"></a>Estado de usuario del host de servicio

El [host de servicio](service-host.md) permite que una aplicación asocie datos de estado con ámbito en el nivel de host de servicio. Este estado se especifica mediante una estructura [**WS \_ SERVICE \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) que se pasa a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) cuando la aplicación crea un [host](service-host.md)de servicio , como se muestra en el ejemplo siguiente.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


Los datos de estado están disponibles para todas las devoluciones de llamada de host de servicio y [las operaciones de servicio](service-operation.md). Las devoluciones de llamada y las operaciones de servicio recuperan la información llamando a la función [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) y especificando el contexto, al que hace referencia la estructura [CONTEXT de WS \_ \_ OPERATION,](ws-operation-context.md) y la propiedad context, como uno de los valores de la eunumeración HOST USER [**\_ \_ \_ \_ \_ \_ STATE de WS OPERATION CONTEXT PROPERTY,**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) como se muestra en el ejemplo siguiente.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




