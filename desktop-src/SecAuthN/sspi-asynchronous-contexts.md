---
title: Contextos asincrónicos
description: Información general de los contextos asincrónicos y el encabezado SSPI asincrónico.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361058"
---
# <a name="asynchronous-contexts"></a><span data-ttu-id="e7e4f-103">Contextos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="e7e4f-103">Asynchronous Contexts</span></span>

<span data-ttu-id="e7e4f-104">Los contextos de seguridad SSPI asincrónicos permiten que los llamadores continúen sin bloquear y recibir notificaciones una vez que se complete la llamada.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-104">Asynchronous SSPI security contexts allow callers to proceed without blocking and receive notifications once the call completes.</span></span> <span data-ttu-id="e7e4f-105">Actualmente, los contextos asincrónicos solo se admiten en servidores y clientes TLS de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-105">Asynchronous contexts are currently only supported for kernel-mode TLS clients and servers.</span></span> <span data-ttu-id="e7e4f-106">Las siguientes funciones SSPI asincrónicas operan en contextos de seguridad asincrónicos:</span><span class="sxs-lookup"><span data-stu-id="e7e4f-106">The following asynchronous SSPI functions operate on asynchronous security contexts:</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="e7e4f-107">Tipos de administración de contexto asincrónico</span><span class="sxs-lookup"><span data-stu-id="e7e4f-107">Async context management types</span></span>

| <span data-ttu-id="e7e4f-108">Nombre de objeto</span><span class="sxs-lookup"><span data-stu-id="e7e4f-108">Object Name</span></span> | <span data-ttu-id="e7e4f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7e4f-109">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="e7e4f-110">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="e7e4f-110">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="e7e4f-111">Devolución de llamada usada para notificar la finalización de una llamada SSPI asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-111">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="e7e4f-112">Funciones de administración de contexto Async</span><span class="sxs-lookup"><span data-stu-id="e7e4f-112">Async context management functions</span></span>

| <span data-ttu-id="e7e4f-113">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="e7e4f-113">API Name</span></span> | <span data-ttu-id="e7e4f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7e4f-114">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="e7e4f-115">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="e7e4f-115">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="e7e4f-116">Crea una instancia de SspiAsyncContext que se usa para realizar el seguimiento de la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-116">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="e7e4f-117">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="e7e4f-117">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="e7e4f-118">Marca un contexto asincrónico para reutilizarlo.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-118">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="e7e4f-119">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="e7e4f-119">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="e7e4f-120">Registra una devolución de llamada a la que se notifica en la finalización de la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-120">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="e7e4f-121">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="e7e4f-121">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="e7e4f-122">Determina si un contexto asincrónico determinado requiere una notificación de la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-122">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="e7e4f-123">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="e7e4f-123">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="e7e4f-124">Obtiene el estado actual de una llamada asincrónica asociada al contexto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-124">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="e7e4f-125">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="e7e4f-125">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="e7e4f-126">Libera un contexto creado en la llamada a la función SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-126">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="e7e4f-127">Funciones SSPI asincrónicas</span><span class="sxs-lookup"><span data-stu-id="e7e4f-127">Async SSPI functions</span></span>

<span data-ttu-id="e7e4f-128">Las siguientes funciones aceptan un contexto asincrónico además de todos los mismos parámetros que su homólogo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-128">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="e7e4f-129">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="e7e4f-129">API Name</span></span> | <span data-ttu-id="e7e4f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7e4f-130">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="e7e4f-131">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="e7e4f-131">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="e7e4f-132">Adquiere de forma asincrónica un identificador a las credenciales preexistentes de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-132">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="e7e4f-133">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="e7e4f-133">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="e7e4f-134">Permite que el componente de servidor de una aplicación de transporte establezca de forma asincrónica un contexto de seguridad entre el servidor y un cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-134">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="e7e4f-135">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="e7e4f-135">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="e7e4f-136">Inicializa un contexto de seguridad Async.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-136">Initializes an async security context.</span></span> |
| [<span data-ttu-id="e7e4f-137">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="e7e4f-137">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="e7e4f-138">Elimina las estructuras de datos locales asociadas al contexto de seguridad especificado Iniciado por una llamada anterior a la función SspiInitializeSecurityContextAsync o la función SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-138">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="e7e4f-139">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="e7e4f-139">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="e7e4f-140">Libera un identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-140">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="e7e4f-141">Ejemplo de API</span><span class="sxs-lookup"><span data-stu-id="e7e4f-141">API Sample</span></span>

<span data-ttu-id="e7e4f-142">Un flujo de llamadas típico funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e7e4f-142">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="e7e4f-143">Crear contexto de SspiAsyncContext para realizar un seguimiento de la llamada mediante [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="e7e4f-143">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="e7e4f-144">Registrar un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para el contexto</span><span class="sxs-lookup"><span data-stu-id="e7e4f-144">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="e7e4f-145">Hacer la llamada asincrónica mediante [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="e7e4f-145">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="e7e4f-146">En la devolución de llamada, recupere el resultado mediante [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="e7e4f-146">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="e7e4f-147">Elimine SspiAsyncContext con [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="e7e4f-147">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="e7e4f-148">Si reutiliza el contexto con [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), vuelva al paso 2.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-148">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="e7e4f-149">En el ejemplo siguiente se muestra una invocación de SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-149">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="e7e4f-150">El ejemplo espera a que se complete la llamada y recupera el resultado.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-150">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="e7e4f-151">En un protocolo de enlace SSPI completo, se llamará a SspiAcceptSecurityContextAsync y SspiInitializeSecurityContextAsync varias veces hasta que se devuelva SEC_E_OK.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-151">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="e7e4f-152">SspiReinitAsyncContext se ha proporcionado para facilitar el uso y facilitar el rendimiento en este caso.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-152">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="e7e4f-153">Las aserciones se utilizan para resaltar lo que se esperaría en caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="e7e4f-153">Asserts are used to highlight what we would expect in the case of success.</span></span>

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a><span data-ttu-id="e7e4f-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7e4f-154">See Also</span></span>

[<span data-ttu-id="e7e4f-155">encabezado SSPI. h</span><span class="sxs-lookup"><span data-stu-id="e7e4f-155">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="e7e4f-156">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="e7e4f-156">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="e7e4f-157">Estructuras SSPI</span><span class="sxs-lookup"><span data-stu-id="e7e4f-157">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


