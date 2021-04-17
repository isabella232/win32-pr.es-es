---
title: Estado de usuario de host de servicio
description: El host de servicio permite a una aplicación asociar datos de Estado cuyo ámbito es el nivel de host del servicio.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Servicios Web de estado de host de usuario para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105705077"
---
# <a name="service-host-user-state"></a><span data-ttu-id="48e5d-106">Estado de usuario de host de servicio</span><span class="sxs-lookup"><span data-stu-id="48e5d-106">Service Host User State</span></span>

<span data-ttu-id="48e5d-107">El [host de servicio](service-host.md) permite a una aplicación asociar datos de Estado cuyo ámbito es el nivel de host del servicio.</span><span class="sxs-lookup"><span data-stu-id="48e5d-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="48e5d-108">Este estado se especifica mediante una estructura [**de \_ \_ propiedades de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) que se pasa a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) cuando la aplicación crea un [host de servicio](service-host.md), tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="48e5d-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="48e5d-109">Los datos de estado están disponibles para todas las devoluciones de llamada y [operaciones de servicio](service-operation.md)del host de servicio.</span><span class="sxs-lookup"><span data-stu-id="48e5d-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="48e5d-110">Las devoluciones de llamada y las operaciones de servicio recuperan la información mediante una llamada a la función [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) y especificando el contexto, al que hace referencia la estructura de contexto de la [ \_ operación \_ WS](ws-operation-context.md) , y la propiedad de contexto, como uno de los valores de la propiedad de contexto de la [**operación WS de \_ \_ \_ \_ \_ \_ Estado de usuario**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="48e5d-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




