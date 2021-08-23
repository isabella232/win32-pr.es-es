---
title: Operaciones de servicio del lado cliente
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Más información sobre: Operaciones de servicio del lado cliente'
keywords:
- Servicios web de operaciones de servicio del lado cliente para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657305"
---
# <a name="client-side-service-operations"></a>Operaciones de servicio del lado cliente

A continuación se muestra el diseño de una operación de servicio del lado cliente:

-   [WS \_ SERVICE \_ PROXY](ws-service-proxy.md) \* serviceProxy: el [proxy de servicio](service-proxy.md) para la llamada.
-   [WS \_ Montón de](ws-heap.md) MONTÓN: un montón necesario que se usa para la serialización del cuerpo y \* la deserialización de [WS \_ MESSAGE](ws-message.md).
-   Parámetros de operaciones de servicio: parámetros pertenecientes a la operación de servicio.
-   [**Propiedades de llamada y su recuento:**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)matriz de propiedades de llamada.
-   [**Recuento de**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) propiedades de llamada: recuento de propiedades de llamada.
-   [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: contexto asincrónico para ejecutar la llamada de forma asincrónica.
-   [WS \_ Error](ws-error.md) de error: objeto de error enriquecido.


### <a name="signature-for-client-side-service-operations"></a>Firma para las operaciones de servicio del lado cliente

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

La llamada a la operación de servicio toma un [ \_ MONTÓN de WS como](ws-heap.md) \* parámetro. Se trata de un parámetro necesario que se usa para la serialización y deserialización de cuerpos de mensaje en parámetros.

La aplicación debe llamar a [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) tanto si la llamada se ha llamado correctamente como si no. Si la llamada se ha hecho correctamente y tiene parámetros de salida, la aplicación debe llamar a **WsResetHeap** inmediatamente después de finalizar con los parámetros de salida.

La aplicación debe asignar memoria para los parámetros de entrada y salida [**con WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Es posible que el proxy de servicio tenga que volver asignárlos para que se sobrescriban los punteros proporcionados. Si se intenta liberar dicha memoria, la aplicación se bloqueará.

### <a name="client-side-service-operation-and-ws_heap"></a>Operación de servicio del lado cliente y WS \_ HEAP

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

-   Obtenga información de error completa si se produce un error durante la llamada a la operación de servicio.
-   Obtenga el objeto de error si el servicio devolvió un error. El error está contenido en el objeto de error. En este caso, el **valor HRESULT** devuelto por la operación de servicio es **WS \_ E ENDPOINT \_ FAULT \_ \_ RECEIVED** (vea Windows valores devueltos [de servicios web](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Propiedades de llamada para las operaciones de servicio del lado cliente

Las propiedades de llamada permiten a una aplicación especificar la configuración personalizada para una llamada determinada. Actualmente, solo hay disponible una propiedad de llamada con el modelo de servicio, [**WS \_ CALL PROPERTY CALL \_ \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

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

A menudo es conveniente abandonar los resultados de una llamada para volver a devolver el control a la aplicación, de modo que la infraestructura controle la finalización real de la llamada. El proxy de servicio proporciona esta instalación a través [**de WsAbandoneCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Tenga en cuenta que el control al autor de la llamada no se puede devolver inmediatamente, la única garantía que ofrece el tiempo de ejecución del proxy de servicio es que no esperaría a que se completara ninguna operación enlazada a E/S antes de devolver el control al autor de la llamada.

Las llamadas en una operación de servicio del lado cliente se pueden abandonar mediante una llamada a [**WsAbanidoCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Toma un proxy de servicio y un identificador de llamada. Un identificador de llamada se proporciona como parte de las propiedades de una llamada en una operación de servicio.

Si el identificador de llamada es 0, el proxy de servicio abandonará todas las llamadas pendientes en esa instancia.

### <a name="call-timeouts"></a>Tiempos de espera de llamada

De forma predeterminada, un proxy de servicio tiene un tiempo de espera de 30 segundos para cada llamada. La propiedad de proxy de servicio [**WS \_ PROXY PROPERTY \_ CALL \_ \_ TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) puede cambiar el tiempo de espera de una llamada al crear un proxy de servicio a través [**de WsCreateServiceProxy.**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)

Una vez alcanzado el tiempo de espera, se abandona la llamada.

### <a name="return-values"></a>Valores devueltos

Todos los **valores HRESULT correctos** deben tratarse como correctos y todos los valores de error deben tratarse como errores. Estos son algunos de los valores **HRESULT** que una aplicación puede esperar:

-   **WS \_ S \_ ASYNC:** la llamada se completará de forma asincrónica.
-   NOERROR: la llamada se completó correctamente.
-   **WS \_ E \_ OPERATION \_ ABANDONED:** la llamada se ha abandonado. El objeto de error contiene el motivo del abandono.
-   **WS \_ E \_ INVALID \_ OPERATION**: el proxy de servicio no está en un estado adecuado para realizar una llamada, compruebe el estado del proxy de servicio para averiguar el estado del proxy de servicio.

Para obtener una lista completa de los valores devueltos, [vea Windows valores devueltos de servicios web.](windows-web-services-return-values.md)

### <a name="code-examples"></a>Ejemplos de código

Para obtener ejemplos de código, vea lo siguiente:

-   [CallAbandoneExample](callabandonexample.md)
-   [**WsAbandoneCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




