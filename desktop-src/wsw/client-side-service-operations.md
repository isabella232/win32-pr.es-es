---
title: Operaciones de servicio del lado cliente
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Más información acerca de: operaciones de servicio del lado cliente'
keywords:
- Servicios Web de operaciones de servicio del lado cliente para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277756"
---
# <a name="client-side-service-operations"></a>Operaciones de servicio del lado cliente

El siguiente es el diseño de una operación de servicio del lado cliente:

-   [WS \_ \_Proxy de servicio](ws-service-proxy.md) \* serviceProxy: el [proxy de servicio](service-proxy.md) de la llamada.
-   [WS \_ Montón del montón](ws-heap.md) \* : montón necesario que se usa para la serialización y deserialización del cuerpo del [ \_ mensaje de WS](ws-message.md).
-   Parámetros de operaciones de servicio: parámetros que pertenecen a la operación de servicio.
-   [**Llamar a las propiedades y su recuento**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): una matriz de propiedades de llamada.
-   Recuento de propiedades de [**llamada**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : recuento de propiedades de llamada.
-   [**WS \_ AsyncContext de \_ contexto asincrónico**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) : contexto asincrónico para ejecutar la llamada de forma asincrónica.
-   [WS \_ Error: objeto de error enriquecido](ws-error.md) .


### <a name="signature-for-client-side-service-operations"></a>Firma para operaciones de servicio del lado cliente

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Consideraciones de memoria para las operaciones de servicio del lado cliente

La llamada a la operación de servicio toma [un \_ montón WS](ws-heap.md) \* como parámetro. Se trata de un parámetro necesario que se usa para la serialización/deserialización de cuerpos de mensaje en parámetros.

La aplicación debe llamar a [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) si la llamada se realizó correctamente o no. Si la llamada se realizó correctamente y tiene parámetros de salida, la aplicación debe llamar a **WsResetHeap** inmediatamente después de que termine con los parámetros de salida.

La aplicación debe asignar memoria para los parámetros in y out con [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Es posible que el proxy de servicio necesite reasignarlos, por lo que se sobrescribirán los punteros proporcionados. Un intento de liberar dicha memoria hará que se bloquee la aplicación.

### <a name="client-side-service-operation-and-ws_heap"></a>Operación de servicio del lado cliente y \_ montón WS

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a>Parámetro de error

La aplicación siempre debe pasar el parámetro de error a:

-   Obtiene información de error enriquecida si se produce un error durante la llamada de operación de servicio.
-   Obtiene el objeto de error si el servicio devuelve un error. El error se encuentra en el objeto de error. En este caso, el valor **HRESULT** devuelto de la operación de servicio es **WS \_ E \_ Endpoint \_ error \_ Received** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Propiedades de llamada para operaciones de servicio del lado cliente

Las propiedades de llamada permiten a una aplicación especificar la configuración personalizada para una llamada determinada. Actualmente, solo hay una propiedad Call disponible con el modelo de servicio, el ID. de llamada de la [**\_ \_ propiedad \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a>Abandonar una llamada

A menudo, es deseable abandonar los resultados de una llamada para devolver el control a la aplicación, de modo que la infraestructura esté administrando la finalización de la llamada real. Proxy de servicio proporciona esta instalación a través de [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Tenga en cuenta que es posible que el control al autor de la llamada no se devuelva inmediatamente, la única garantía de que el tiempo de ejecución del proxy de servicio proporciona es que no esperará a que se complete la operación enlazada de e/s antes de devolver el control al autor de la llamada.

Las llamadas en una operación de servicio del lado cliente se pueden abandonar por medio de una llamada a [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Toma un proxy de servicio y un identificador de llamada. Un identificador de llamada se proporciona como parte de las propiedades de una llamada en una operación de servicio.

Si el ID. de llamada es 0, el proxy de servicio abandonará todas las llamadas pendientes en esa instancia.

### <a name="call-timeouts"></a>Tiempos de espera de llamadas

De forma predeterminada, un proxy de servicio tiene un tiempo de espera de 30 segundos para cada llamada. El tiempo de espera de una llamada se puede cambiar mediante la propiedad proxy del servicio de tiempo de espera de la llamada [](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)de propiedad del proxy de [**WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) al crear un proxy de servicio a través de WsCreateServiceProxy.

Una vez alcanzado el tiempo de espera, se abandona la llamada.

### <a name="return-values"></a>Valores devueltos

Todos los valores **HRESULT** correctos se deben tratar como correctos y todos los valores de error se deben tratar como errores. A continuación se muestran algunos de los valores **HRESULT** que una aplicación puede esperar:

-   **WS \_ S \_ Async**: la llamada se completará de forma asincrónica.
-   NoError: la llamada se completó correctamente.
-   **WS \_ \_Operación E \_ abandonada**: se abandonó la llamada. El objeto error contiene el motivo del abandono.
-   **WS \_ E \_ \_ operación no válida**: el proxy de servicio no tiene un estado adecuado para realizar una llamada, compruebe el estado del proxy de servicio para averiguar el estado del proxy de servicio.

Para obtener una lista completa de los valores devueltos, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md).

### <a name="code-examples"></a>Ejemplos de código

Para obtener ejemplos de código, vea lo siguiente:

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




