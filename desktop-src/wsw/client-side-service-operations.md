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
# <a name="client-side-service-operations"></a><span data-ttu-id="01a91-106">Operaciones de servicio del lado cliente</span><span class="sxs-lookup"><span data-stu-id="01a91-106">Client-side Service Operations</span></span>

<span data-ttu-id="01a91-107">El siguiente es el diseño de una operación de servicio del lado cliente:</span><span class="sxs-lookup"><span data-stu-id="01a91-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="01a91-108">[WS \_ \_Proxy de servicio](ws-service-proxy.md) \* serviceProxy: el [proxy de servicio](service-proxy.md) de la llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="01a91-109">[WS \_ Montón del montón](ws-heap.md) \* : montón necesario que se usa para la serialización y deserialización del cuerpo del [ \_ mensaje de WS](ws-message.md).</span><span class="sxs-lookup"><span data-stu-id="01a91-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="01a91-110">Parámetros de operaciones de servicio: parámetros que pertenecen a la operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="01a91-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="01a91-111">[**Llamar a las propiedades y su recuento**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): una matriz de propiedades de llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="01a91-112">Recuento de propiedades de [**llamada**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : recuento de propiedades de llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="01a91-113">[**WS \_ AsyncContext de \_ contexto asincrónico**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) : contexto asincrónico para ejecutar la llamada de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="01a91-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="01a91-114">[WS \_ Error: objeto de error enriquecido](ws-error.md) .</span><span class="sxs-lookup"><span data-stu-id="01a91-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="01a91-115">Firma para operaciones de servicio del lado cliente</span><span class="sxs-lookup"><span data-stu-id="01a91-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="01a91-116">Consideraciones de memoria para las operaciones de servicio del lado cliente</span><span class="sxs-lookup"><span data-stu-id="01a91-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="01a91-117">La llamada a la operación de servicio toma [un \_ montón WS](ws-heap.md) \* como parámetro.</span><span class="sxs-lookup"><span data-stu-id="01a91-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="01a91-118">Se trata de un parámetro necesario que se usa para la serialización/deserialización de cuerpos de mensaje en parámetros.</span><span class="sxs-lookup"><span data-stu-id="01a91-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="01a91-119">La aplicación debe llamar a [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) si la llamada se realizó correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="01a91-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="01a91-120">Si la llamada se realizó correctamente y tiene parámetros de salida, la aplicación debe llamar a **WsResetHeap** inmediatamente después de que termine con los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="01a91-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="01a91-121">La aplicación debe asignar memoria para los parámetros in y out con [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span><span class="sxs-lookup"><span data-stu-id="01a91-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="01a91-122">Es posible que el proxy de servicio necesite reasignarlos, por lo que se sobrescribirán los punteros proporcionados.</span><span class="sxs-lookup"><span data-stu-id="01a91-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="01a91-123">Un intento de liberar dicha memoria hará que se bloquee la aplicación.</span><span class="sxs-lookup"><span data-stu-id="01a91-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="01a91-124">Operación de servicio del lado cliente y \_ montón WS</span><span class="sxs-lookup"><span data-stu-id="01a91-124">Client-side Service Operation and WS\_HEAP</span></span>

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

### <a name="error-parameter"></a><span data-ttu-id="01a91-125">Parámetro de error</span><span class="sxs-lookup"><span data-stu-id="01a91-125">Error parameter</span></span>

<span data-ttu-id="01a91-126">La aplicación siempre debe pasar el parámetro de error a:</span><span class="sxs-lookup"><span data-stu-id="01a91-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="01a91-127">Obtiene información de error enriquecida si se produce un error durante la llamada de operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="01a91-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="01a91-128">Obtiene el objeto de error si el servicio devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="01a91-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="01a91-129">El error se encuentra en el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="01a91-129">The fault is contained in the error object.</span></span> <span data-ttu-id="01a91-130">En este caso, el valor **HRESULT** devuelto de la operación de servicio es **WS \_ E \_ Endpoint \_ error \_ Received** (vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="01a91-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="01a91-131">Propiedades de llamada para operaciones de servicio del lado cliente</span><span class="sxs-lookup"><span data-stu-id="01a91-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="01a91-132">Las propiedades de llamada permiten a una aplicación especificar la configuración personalizada para una llamada determinada.</span><span class="sxs-lookup"><span data-stu-id="01a91-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="01a91-133">Actualmente, solo hay una propiedad Call disponible con el modelo de servicio, el ID. de llamada de la [**\_ \_ propiedad \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span><span class="sxs-lookup"><span data-stu-id="01a91-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

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

### <a name="abandoning-a-call"></a><span data-ttu-id="01a91-134">Abandonar una llamada</span><span class="sxs-lookup"><span data-stu-id="01a91-134">Abandoning a Call</span></span>

<span data-ttu-id="01a91-135">A menudo, es deseable abandonar los resultados de una llamada para devolver el control a la aplicación, de modo que la infraestructura esté administrando la finalización de la llamada real.</span><span class="sxs-lookup"><span data-stu-id="01a91-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="01a91-136">Proxy de servicio proporciona esta instalación a través de [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="01a91-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="01a91-137">Tenga en cuenta que es posible que el control al autor de la llamada no se devuelva inmediatamente, la única garantía de que el tiempo de ejecución del proxy de servicio proporciona es que no esperará a que se complete la operación enlazada de e/s antes de devolver el control al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="01a91-138">Las llamadas en una operación de servicio del lado cliente se pueden abandonar por medio de una llamada a [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="01a91-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="01a91-139">Toma un proxy de servicio y un identificador de llamada. Un identificador de llamada se proporciona como parte de las propiedades de una llamada en una operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="01a91-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="01a91-140">Si el ID. de llamada es 0, el proxy de servicio abandonará todas las llamadas pendientes en esa instancia.</span><span class="sxs-lookup"><span data-stu-id="01a91-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="01a91-141">Tiempos de espera de llamadas</span><span class="sxs-lookup"><span data-stu-id="01a91-141">Call Timeouts</span></span>

<span data-ttu-id="01a91-142">De forma predeterminada, un proxy de servicio tiene un tiempo de espera de 30 segundos para cada llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="01a91-143">El tiempo de espera de una llamada se puede cambiar mediante la propiedad proxy del servicio de tiempo de espera de la llamada [](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)de propiedad del proxy de [**WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) al crear un proxy de servicio a través de WsCreateServiceProxy.</span><span class="sxs-lookup"><span data-stu-id="01a91-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="01a91-144">Una vez alcanzado el tiempo de espera, se abandona la llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="01a91-145">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="01a91-145">Return Values</span></span>

<span data-ttu-id="01a91-146">Todos los valores **HRESULT** correctos se deben tratar como correctos y todos los valores de error se deben tratar como errores.</span><span class="sxs-lookup"><span data-stu-id="01a91-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="01a91-147">A continuación se muestran algunos de los valores **HRESULT** que una aplicación puede esperar:</span><span class="sxs-lookup"><span data-stu-id="01a91-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="01a91-148">**WS \_ S \_ Async**: la llamada se completará de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="01a91-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="01a91-149">NoError: la llamada se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="01a91-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="01a91-150">**WS \_ \_Operación E \_ abandonada**: se abandonó la llamada.</span><span class="sxs-lookup"><span data-stu-id="01a91-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="01a91-151">El objeto error contiene el motivo del abandono.</span><span class="sxs-lookup"><span data-stu-id="01a91-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="01a91-152">**WS \_ E \_ \_ operación no válida**: el proxy de servicio no tiene un estado adecuado para realizar una llamada, compruebe el estado del proxy de servicio para averiguar el estado del proxy de servicio.</span><span class="sxs-lookup"><span data-stu-id="01a91-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="01a91-153">Para obtener una lista completa de los valores devueltos, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="01a91-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="01a91-154">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="01a91-154">Code Examples</span></span>

<span data-ttu-id="01a91-155">Para obtener ejemplos de código, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="01a91-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="01a91-156">CallAbandonExample</span><span class="sxs-lookup"><span data-stu-id="01a91-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="01a91-157">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="01a91-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




