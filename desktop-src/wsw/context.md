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
# <a name="context-windows-web-services"></a><span data-ttu-id="fbf10-106">Contexto (servicios Web de Windows)</span><span class="sxs-lookup"><span data-stu-id="fbf10-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="fbf10-107">Se usa un contexto en [las operaciones](service-operation.md) de servicio de modelo de servicio y las devoluciones de llamada para pasar datos de estado pertinentes a la operación de servicio o devolución de llamada cuando se invoca.</span><span class="sxs-lookup"><span data-stu-id="fbf10-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="fbf10-108">Una estructura de [ \_ \_ contexto de operación WS](ws-operation-context.md) hace referencia a un contexto.</span><span class="sxs-lookup"><span data-stu-id="fbf10-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="fbf10-109">Las propiedades de un contexto se pueden recuperar con la función [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="fbf10-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="fbf10-110">No todas las propiedades de contexto están disponibles en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="fbf10-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="fbf10-111">Vea la documentación de la propiedad de contexto relativa a la disponibilidad de una propiedad específica en una devolución de llamada o una [operación de servicio](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="fbf10-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="fbf10-112">Para obtener más información sobre cómo mantener la duración y el subprocesamiento de los contextos de la operación, vea el tema [duración del contexto de operación y subprocesamiento](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf10-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="fbf10-113">La enumeración siguiente forma parte del contexto:</span><span class="sxs-lookup"><span data-stu-id="fbf10-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="fbf10-114">**identificador de la propiedad de contexto de \_ operación WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fbf10-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="fbf10-115">La siguiente función forma parte del contexto:</span><span class="sxs-lookup"><span data-stu-id="fbf10-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="fbf10-116">**WsGetOperationContextProperty**</span><span class="sxs-lookup"><span data-stu-id="fbf10-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="fbf10-117">El siguiente identificador forma parte del contexto:</span><span class="sxs-lookup"><span data-stu-id="fbf10-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="fbf10-118">\_contexto de operación WS \_</span><span class="sxs-lookup"><span data-stu-id="fbf10-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




