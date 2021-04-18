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
# <a name="server-side-service-operations"></a><span data-ttu-id="a88d5-106">Operaciones de servicio del lado servidor</span><span class="sxs-lookup"><span data-stu-id="a88d5-106">Server Side Service Operations</span></span>

<span data-ttu-id="a88d5-107">En esta sección se describen las operaciones de servicio del lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88d5-107">This section describes service side service operations.</span></span>


<span data-ttu-id="a88d5-108">El siguiente es el diseño de una operación de servicio del lado servidor</span><span class="sxs-lookup"><span data-stu-id="a88d5-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="a88d5-109">contexto de la [ \_ \_ operación const WS](ws-operation-context.md) \* : el [contexto](context.md)de la operación.</span><span class="sxs-lookup"><span data-stu-id="a88d5-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="a88d5-110">Parámetros de operaciones de servicio: parámetros que pertenecen a la operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88d5-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="a88d5-111">[**Async WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext: contexto asincrónico para ejecutar las operaciones de servicio de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a88d5-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="a88d5-112">[WS \_ ](ws-error.md) \* Error: objeto de error enriquecido.</span><span class="sxs-lookup"><span data-stu-id="a88d5-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

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

## <a name="fault-and-error-handling"></a><span data-ttu-id="a88d5-113">Control de errores y errores</span><span class="sxs-lookup"><span data-stu-id="a88d5-113">Fault And Error Handling</span></span>

<span data-ttu-id="a88d5-114">El lado del servidor debe utilizar errores para proporcionar condiciones de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="a88d5-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="a88d5-115">Para ello, puede devolver un valor HRESULT con errores e insertar el error en el objeto de error.</span><span class="sxs-lookup"><span data-stu-id="a88d5-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="a88d5-116">Si el error no se establece en el objeto de error y se devuelve un error HRESULT, la infraestructura intentará devolver un error al cliente.</span><span class="sxs-lookup"><span data-stu-id="a88d5-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="a88d5-117">El nivel de detalles que se revela al cliente en este caso se controla mediante la propiedad servicio de divulgación de errores de la [**\_ propiedad de servicio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) en el [host del servicio](service-host.md).</span><span class="sxs-lookup"><span data-stu-id="a88d5-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="a88d5-118">Finalización de llamada</span><span class="sxs-lookup"><span data-stu-id="a88d5-118">Call Completion</span></span>

<span data-ttu-id="a88d5-119">Se dice que una llamada en una operación de servicio del lado servidor sincrónica se ha completado cuando devuelve el control al host del servicio.</span><span class="sxs-lookup"><span data-stu-id="a88d5-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="a88d5-120">En el caso de una operación de servicio asincrónica, una llamada se considera completada una vez que la notificación de devolución de llamada la emite la implementación de la operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88d5-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="a88d5-121">Duración de la llamada</span><span class="sxs-lookup"><span data-stu-id="a88d5-121">Call Lifetime</span></span>

<span data-ttu-id="a88d5-122">Se debe tener especial cuidado al implementar una operación de servicio en el servidor sobre su duración.</span><span class="sxs-lookup"><span data-stu-id="a88d5-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="a88d5-123">La duración de una llamada puede afectar en gran medida al tiempo que tarda el host del servicio en cerrarse.</span><span class="sxs-lookup"><span data-stu-id="a88d5-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="a88d5-124">Si se espera que una operación de servicio en el servidor se bloquee debido a una operación enlazada de e/s, se recomienda que registre una devolución de llamada de cancelación para que se le notifique si el host del servicio se anula o cuando el cliente cierra la conexión subyacente.</span><span class="sxs-lookup"><span data-stu-id="a88d5-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="a88d5-125">Consideración de las operaciones del servicio del servidor y de la memoria</span><span class="sxs-lookup"><span data-stu-id="a88d5-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="a88d5-126">Si una operación de servicio necesita asignar memoria para sus parámetros salientes, debe usar el objeto de [ \_ montón WS](ws-heap.md) disponible en el [ \_ \_ contexto de la operación WS](ws-operation-context.md).</span><span class="sxs-lookup"><span data-stu-id="a88d5-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="a88d5-127">Ejemplo: operación de servicio y \_ montón de WS</span><span class="sxs-lookup"><span data-stu-id="a88d5-127">Example: Service Operation and WS\_HEAP</span></span>

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

## <a name="return-values"></a><span data-ttu-id="a88d5-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a88d5-128">Return Values</span></span>

-   <span data-ttu-id="a88d5-129">WS \_ S \_ Async: la llamada se completará en Async.</span><span class="sxs-lookup"><span data-stu-id="a88d5-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="a88d5-130">WS \_ S \_ End: la llamada se completó correctamente, el servidor no espera ningún [ \_ mensaje WS](ws-message.md) del cliente más allá de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a88d5-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="a88d5-131">Si llega otro \_ mensaje WS, el servidor debería anular el canal.</span><span class="sxs-lookup"><span data-stu-id="a88d5-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="a88d5-132">NoError/todos los demás valores HRESULT correctos: llamada completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a88d5-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="a88d5-133">Tenga en cuenta que se recomienda que la aplicación no devuelva HRESULT, y que no se haya podido completar correctamente la operación de servicio.</span><span class="sxs-lookup"><span data-stu-id="a88d5-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="a88d5-134">Todo con un error HRESULT: un error se devuelve al cliente si hay uno disponible en WS \_ error.</span><span class="sxs-lookup"><span data-stu-id="a88d5-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="a88d5-135">De lo contrario, se devuelve un error genérico al cliente.</span><span class="sxs-lookup"><span data-stu-id="a88d5-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="a88d5-136">Vea la explicación del error anterior.</span><span class="sxs-lookup"><span data-stu-id="a88d5-136">See fault discussion above.</span></span>

<span data-ttu-id="a88d5-137">Consulte [cancelación de llamadas](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="a88d5-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




