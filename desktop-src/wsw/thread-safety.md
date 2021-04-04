---
title: Seguridad para subprocesos
description: Todas las funciones de esta API son seguras para llamar a la vez desde subprocesos diferentes. Sin embargo, cada objeto que se pasa como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, tal y como se describe a continuación.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servicios Web de seguridad para subprocesos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797289"
---
# <a name="thread-safety"></a><span data-ttu-id="35735-107">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="35735-107">Thread Safety</span></span>

<span data-ttu-id="35735-108">Todas las funciones de esta API son seguras para llamar a la vez desde subprocesos diferentes.</span><span class="sxs-lookup"><span data-stu-id="35735-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="35735-109">Sin embargo, cada objeto que se pasa como parámetro a las funciones tiene un comportamiento de subprocesamiento específico, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="35735-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="35735-110">Los siguientes identificadores son de un solo subproceso y no admiten operaciones simultáneas para una instancia determinada:</span><span class="sxs-lookup"><span data-stu-id="35735-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="35735-111">\_montón WS</span><span class="sxs-lookup"><span data-stu-id="35735-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="35735-112">\_mensaje WS</span><span class="sxs-lookup"><span data-stu-id="35735-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="35735-113">búfer de WS \_ XML \_</span><span class="sxs-lookup"><span data-stu-id="35735-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="35735-114">\_lector de XML de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="35735-115">\_escritor de XML de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="35735-116">ERROR de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="35735-117">\_contexto de operación WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="35735-118">Directiva de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="35735-119">metadatos de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="35735-120">\_token de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="35735-121">\_contexto de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="35735-122">Los siguientes identificadores son de subprocesamiento libre y admiten operaciones simultáneas para una instancia determinada:</span><span class="sxs-lookup"><span data-stu-id="35735-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="35735-123">canal de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="35735-124">agente de escucha de WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="35735-125">\_host de servicio WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="35735-126">\_proxy de servicio WS \_</span><span class="sxs-lookup"><span data-stu-id="35735-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="35735-127">Para todos estos identificadores, los subprocesos se definen en términos de operaciones (no llamadas a función).</span><span class="sxs-lookup"><span data-stu-id="35735-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="35735-128">Una operación se define de forma diferente para las funciones invocadas sincrónicamente frente a las funciones invocadas de forma asincrónica:</span><span class="sxs-lookup"><span data-stu-id="35735-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="35735-129">En el caso de las funciones invocadas sincrónicamente, la operación está pendiente durante la ejecución de la función.</span><span class="sxs-lookup"><span data-stu-id="35735-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="35735-130">En el caso de las funciones invocadas de forma asincrónica, si la función devuelve un código de retorno distinto de **WS \_ S \_ Async** , la operación está pendiente durante la ejecución de la función.</span><span class="sxs-lookup"><span data-stu-id="35735-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="35735-131">Sin embargo, si la función devuelve **WS \_ S \_ Async** , la operación está pendiente hasta que se invoca la [**devolución de \_ \_ llamada de WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="35735-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="35735-132">Para obtener más información sobre cómo invocar funciones de forma asincrónica, vea el tema sobre el [modelo asincrónico](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="35735-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="35735-133">Para ver los códigos de error, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="35735-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="35735-134">Si no se sigue el contrato de subprocesos de un objeto, se producirá un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="35735-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




