---
title: Cancelación de llamada
description: La notificación de cancelación de llamada cancela el funcionamiento de las operaciones de servicio del lado servidor y las devoluciones de llamada del modelo de servicio.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Llamar a servicios Web de cancelación para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105695808"
---
# <a name="call-cancellation"></a><span data-ttu-id="a4c6d-106">Cancelación de llamada</span><span class="sxs-lookup"><span data-stu-id="a4c6d-106">Call cancellation</span></span>

<span data-ttu-id="a4c6d-107">La notificación de cancelación de llamada cancela el funcionamiento de [las operaciones de servicio del lado servidor y las](server-side-service-operations.md) devoluciones de llamada del modelo de servicio.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="a4c6d-108">Dicha cancelación puede ser por uno de estos dos motivos:</span><span class="sxs-lookup"><span data-stu-id="a4c6d-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="a4c6d-109">El host de servicio ha detenido las operaciones debido a una llamada a la función [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .</span><span class="sxs-lookup"><span data-stu-id="a4c6d-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="a4c6d-110">El canal subyacente ha generado un error.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="a4c6d-111">Para recibir una notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio deben registrar una devolución de [](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) llamada de [**devolución de llamada de \_ cancelación de operación \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) llamando a la función WsRegisterOperationForCancel.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="a4c6d-112">Opcionalmente, como parte del registro de la notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio también puede registrar datos de estado específicos de la aplicación y la devolución de llamada de [**\_ devolución de \_ \_ \_ llamada de estado de la operación WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .</span><span class="sxs-lookup"><span data-stu-id="a4c6d-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="a4c6d-113">Los datos de estado se ponen a disposición de la devolución de llamada de cancelación de la [**\_ operación \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) .</span><span class="sxs-lookup"><span data-stu-id="a4c6d-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="a4c6d-114">Al finalizar la llamada, se llama a la devolución de llamada de devolución de llamada de estado de la [**\_ operación \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) para ofrecer a la aplicación la oportunidad de liberar los datos de estado.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="a4c6d-115">Para obtener un ejemplo de código, vea [BlockingServiceExample](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="a4c6d-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="a4c6d-116">Solo se llama una vez a la devolución de llamada de cancelación para la duración de las [operaciones del servicio del servidor](server-side-service-operations.md) o de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="a4c6d-117">La cancelación de llamadas está disponible en para todas las devoluciones de llamada de host de servicio que toman el [ \_ \_ contexto de operación WS](ws-operation-context.md) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="a4c6d-118">Los siguientes elementos de la API se relacionan con la cancelación de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="a4c6d-119">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="a4c6d-119">Callback</span></span>                                                                         | <span data-ttu-id="a4c6d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4c6d-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4c6d-121">**\_devolución de \_ llamada de cancelación de operación WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4c6d-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="a4c6d-122">Invocado por el modelo de servicio para notificar la cancelación de una operación de servicio asincrónica como resultado de un cierre del host de servicio anulado.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="a4c6d-123">**\_devolución de \_ \_ llamada de estado libre de operación WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4c6d-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="a4c6d-124">Invocado por el modelo de servicio para permitir que una aplicación Limpie los datos de estado que se registraron con la devolución de llamada de cancelación.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="a4c6d-125">Función</span><span class="sxs-lookup"><span data-stu-id="a4c6d-125">Function</span></span>                                                             | <span data-ttu-id="a4c6d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4c6d-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4c6d-127">**WsRegisterOperationForCancel**</span><span class="sxs-lookup"><span data-stu-id="a4c6d-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="a4c6d-128">Permite a una operación de servicio o a una devolución de llamada del modelo de servicio registrarse para una notificación de cancelación.</span><span class="sxs-lookup"><span data-stu-id="a4c6d-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




