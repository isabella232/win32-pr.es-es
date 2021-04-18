---
title: Operaciones de servicio del lado servidor
description: En esta sección se describen las operaciones de servicio del lado de servicio.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Servicios Web de operaciones de servicio del lado servidor para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421631"
---
# <a name="server-side-service-operations"></a>Operaciones de servicio del lado servidor

En esta sección se describen las operaciones de servicio del lado de servicio.


El siguiente es el diseño de una operación de servicio del lado servidor

-   contexto de la [ \_ \_ operación const WS](ws-operation-context.md) \* : el [contexto](context.md)de la operación.
-   Parámetros de operaciones de servicio: parámetros que pertenecen a la operación de servicio.
-   [**Async WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto asincrónico para ejecutar las operaciones de servicio de forma asincrónica.
-   [WS \_ ](ws-error.md) \* Error: objeto de error enriquecido.

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a>Control de errores y errores

El lado del servidor debe utilizar errores para proporcionar condiciones de error al cliente. Para ello, puede devolver un valor HRESULT con errores e insertar el error en el objeto de error.

Si el error no se establece en el objeto de error y se devuelve un error HRESULT, la infraestructura intentará devolver un error al cliente. El nivel de detalles que se revela al cliente en este caso se controla mediante la propiedad servicio de divulgación de errores de la [**\_ propiedad de servicio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) en el [host del servicio](service-host.md).

## <a name="call-completion"></a>Finalización de llamada

Se dice que una llamada en una operación de servicio del lado servidor sincrónica se ha completado cuando devuelve el control al host del servicio. En el caso de una operación de servicio asincrónica, una llamada se considera completada una vez que la notificación de devolución de llamada la emite la implementación de la operación de servicio.

## <a name="call-lifetime"></a>Duración de la llamada

Se debe tener especial cuidado al implementar una operación de servicio en el servidor sobre su duración. La duración de una llamada puede afectar en gran medida al tiempo que tarda el host del servicio en cerrarse.

Si se espera que una operación de servicio en el servidor se bloquee debido a una operación enlazada de e/s, se recomienda que registre una devolución de llamada de cancelación para que se le notifique si el host del servicio se anula o cuando el cliente cierra la conexión subyacente.

## <a name="server-side-service-operations-and-memory-consideration"></a>Consideración de las operaciones del servicio del servidor y de la memoria

Si una operación de servicio necesita asignar memoria para sus parámetros salientes, debe usar el objeto de [ \_ montón WS](ws-heap.md) disponible en el [ \_ \_ contexto de la operación WS](ws-operation-context.md).

Ejemplo: operación de servicio y \_ montón de WS

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a>Valores devueltos

-   WS \_ S \_ Async: la llamada se completará en Async.
-   WS \_ S \_ End: la llamada se completó correctamente, el servidor no espera ningún [ \_ mensaje WS](ws-message.md) del cliente más allá de esta llamada. Si llega otro \_ mensaje WS, el servidor debería anular el canal.
-   NoError/todos los demás valores HRESULT correctos: llamada completada correctamente. Tenga en cuenta que se recomienda que la aplicación no devuelva HRESULT, y que no se haya podido completar correctamente la operación de servicio.
-   Todo con un error HRESULT: un error se devuelve al cliente si hay uno disponible en WS \_ error. De lo contrario, se devuelve un error genérico al cliente. Vea la explicación del error anterior.

Consulte [cancelación de llamadas](call-cancellation.md).

 

 




