---
title: Operaciones de servicio del lado servidor
description: En esta sección se describen las operaciones de servicio del lado del servicio.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Servicios web de operaciones de servicio del lado servidor para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1656e56df08d00a0551946c4e52898beccd4d1a37a5bd96c63eb2066928fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344635"
---
# <a name="server-side-service-operations"></a>Operaciones de servicio del lado servidor

En esta sección se describen las operaciones de servicio del lado del servicio.


A continuación se muestra el diseño de una operación de servicio del lado servidor

-   Contexto de [contexto de operación de WS: \_ \_ ](ws-operation-context.md) \* contexto de la [operación](context.md).
-   Parámetros de operaciones de servicio: parámetros pertenecientes a la operación de servicio.
-   const [**WS \_ ASYNC \_ CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto asincrónico para ejecutar las operaciones de servicio de forma asincrónica.
-   [WS \_ Error de](ws-error.md) \* error: objeto de error enriquecido.

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

El lado servidor debe usar errores para entregar condiciones de error al cliente. Para ello, devuelve un HRESULT con errores e inserta el error en el objeto de error.

Si el error no se establece en el objeto de error y se devuelve un HRESULT de error, la infraestructura intentará devolver un error al cliente. El nivel de detalles que se revela al cliente en este caso se controla mediante la propiedad del servicio [**WS \_ SERVICE PROPERTY FAULT \_ \_ \_ DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) en el [host de servicio](service-host.md).

## <a name="call-completion"></a>Finalización de llamadas

Se dice que una llamada en una operación de servicio del lado servidor sincrónica se ha completado cuando alguna de las dos ha devuelto el control al host de servicio. Para una operación de servicio asincrónica, una llamada se considera completada una vez que la implementación de la operación de servicio emite la notificación de devolución de llamada.

## <a name="call-lifetime"></a>Duración de la llamada

Debe tener especial cuidado al implementar una operación de servicio del lado servidor sobre su duración. La duración de una llamada puede afectar en gran medida al tiempo que tarda el host de servicio en apagarse.

Si se espera que una operación de servicio del lado servidor se bloquee debido a alguna operación enlazada a E/S, se recomienda registrar una devolución de llamada de cancelación de modo que se notifique si se anula el host de servicio o cuando el cliente cierra la conexión subyacente.

## <a name="server-side-service-operations-and-memory-consideration"></a>Consideración de memoria y operaciones del servicio del lado servidor

Si una operación de servicio necesita asignar memoria para sus parámetros de salida, debe usar el objeto [ \_ HEAP](ws-heap.md) de WS disponible a través de [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md).

Ejemplo: Operación de servicio y WS \_ HEAP

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

-   WS \_ S \_ ASYNC: la llamada se completará de forma asincrónica.
-   WS S END: la llamada se completó correctamente, el servidor no espera ningún \_ \_ mensaje [WS \_ ](ws-message.md) del cliente más allá de esta llamada. Si aparece otro mensaje \_ WS, el servidor debe anular el canal.
-   NOERROR/All other success HRESULTS: la llamada se completó correctamente. Tenga en cuenta que se recomienda que la aplicación no devuelva HRESULT otro y noerror para completar correctamente la operación de servicio.
-   Todo con un HRESULT de error: se devuelve un error al cliente si hay uno disponible en error de \_ WS. De lo contrario, se envía un error genérico al cliente. Consulte la explicación de errores anterior.

Consulte Cancelación [de llamadas.](call-cancellation.md)

 

 




