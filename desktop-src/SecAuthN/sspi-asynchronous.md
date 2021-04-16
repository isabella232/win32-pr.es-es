---
title: SSPI asincrónico
description: Información general sobre el encabezado SSPI asincrónico.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720658"
---
# <a name="asynchronous-sspi"></a><span data-ttu-id="5fed8-103">SSPI asincrónico</span><span class="sxs-lookup"><span data-stu-id="5fed8-103">Asynchronous SSPI</span></span>

<span data-ttu-id="5fed8-104">El encabezado SSPI asincrónico incluye funciones que admiten objetos de contexto asincrónicos, lo que permite a los autores de llamadas establecer contextos de seguridad entre el servidor y los clientes remotos simultáneamente a través de un ciclo de vida de llamadas asincrónicas de SSPI.</span><span class="sxs-lookup"><span data-stu-id="5fed8-104">The asynchronous SSPI header includes functions that support async context objects, allowing callers to establish security contexts between server and remote clients concurrently through an async SSPI call lifecycle.</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="5fed8-105">Tipos de administración de contexto asincrónico</span><span class="sxs-lookup"><span data-stu-id="5fed8-105">Async context management types</span></span>

| <span data-ttu-id="5fed8-106">Nombre de objeto</span><span class="sxs-lookup"><span data-stu-id="5fed8-106">Object Name</span></span> | <span data-ttu-id="5fed8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fed8-107">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="5fed8-108">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="5fed8-108">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="5fed8-109">Devolución de llamada usada para notificar la finalización de una llamada SSPI asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5fed8-109">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="5fed8-110">Funciones de administración de contexto Async</span><span class="sxs-lookup"><span data-stu-id="5fed8-110">Async context management functions</span></span>

| <span data-ttu-id="5fed8-111">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="5fed8-111">API Name</span></span> | <span data-ttu-id="5fed8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fed8-112">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="5fed8-113">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="5fed8-113">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="5fed8-114">Crea una instancia de SspiAsyncContext que se usa para realizar el seguimiento de la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5fed8-114">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="5fed8-115">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="5fed8-115">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="5fed8-116">Marca un contexto asincrónico para reutilizarlo.</span><span class="sxs-lookup"><span data-stu-id="5fed8-116">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="5fed8-117">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="5fed8-117">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="5fed8-118">Registra una devolución de llamada a la que se notifica en la finalización de la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5fed8-118">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="5fed8-119">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="5fed8-119">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="5fed8-120">Determina si un contexto asincrónico determinado requiere una notificación de la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5fed8-120">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="5fed8-121">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="5fed8-121">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="5fed8-122">Obtiene el estado actual de una llamada asincrónica asociada al contexto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="5fed8-122">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="5fed8-123">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="5fed8-123">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="5fed8-124">Libera un contexto creado en la llamada a la función SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="5fed8-124">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="5fed8-125">Funciones SSPI asincrónicas</span><span class="sxs-lookup"><span data-stu-id="5fed8-125">Async SSPI functions</span></span>

<span data-ttu-id="5fed8-126">Las siguientes funciones aceptan un contexto asincrónico además de todos los mismos parámetros que su homólogo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="5fed8-126">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="5fed8-127">Nombre de la API</span><span class="sxs-lookup"><span data-stu-id="5fed8-127">API Name</span></span> | <span data-ttu-id="5fed8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fed8-128">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="5fed8-129">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="5fed8-129">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="5fed8-130">Adquiere de forma asincrónica un identificador a las credenciales preexistentes de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5fed8-130">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="5fed8-131">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="5fed8-131">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="5fed8-132">Permite que el componente de servidor de una aplicación de transporte establezca de forma asincrónica un contexto de seguridad entre el servidor y un cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="5fed8-132">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="5fed8-133">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="5fed8-133">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="5fed8-134">Inicializa un contexto de seguridad Async.</span><span class="sxs-lookup"><span data-stu-id="5fed8-134">Initializes an async security context.</span></span> |
| [<span data-ttu-id="5fed8-135">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="5fed8-135">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="5fed8-136">Elimina las estructuras de datos locales asociadas al contexto de seguridad especificado Iniciado por una llamada anterior a la función SspiInitializeSecurityContextAsync o la función SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="5fed8-136">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="5fed8-137">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="5fed8-137">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="5fed8-138">Libera un identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="5fed8-138">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="5fed8-139">Ejemplo de API</span><span class="sxs-lookup"><span data-stu-id="5fed8-139">API Sample</span></span>

<span data-ttu-id="5fed8-140">Un flujo de llamadas típico funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5fed8-140">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="5fed8-141">Crear contexto de SspiAsyncContext para realizar un seguimiento de la llamada mediante [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="5fed8-141">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="5fed8-142">Registrar un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para el contexto</span><span class="sxs-lookup"><span data-stu-id="5fed8-142">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="5fed8-143">Hacer la llamada asincrónica mediante [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="5fed8-143">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="5fed8-144">En la devolución de llamada, recupere el resultado mediante [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="5fed8-144">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="5fed8-145">Elimine SspiAsyncContext con [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="5fed8-145">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="5fed8-146">Si reutiliza el contexto con [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), vuelva al paso 2.</span><span class="sxs-lookup"><span data-stu-id="5fed8-146">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="5fed8-147">En el ejemplo siguiente se muestra una invocación de SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="5fed8-147">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="5fed8-148">El ejemplo espera a que se complete la llamada y recupera el resultado.</span><span class="sxs-lookup"><span data-stu-id="5fed8-148">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="5fed8-149">En un protocolo de enlace SSPI completo, se llamará a SspiAcceptSecurityContextAsync y SspiInitializeSecurityContextAsync varias veces hasta que se devuelva SEC_E_OK.</span><span class="sxs-lookup"><span data-stu-id="5fed8-149">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="5fed8-150">SspiReinitAsyncContext se ha proporcionado para facilitar el uso y facilitar el rendimiento en este caso.</span><span class="sxs-lookup"><span data-stu-id="5fed8-150">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="5fed8-151">Las aserciones se utilizan para resaltar lo que se esperaría en caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="5fed8-151">Asserts are used to highlight what we would expect in the case of success.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="5fed8-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fed8-152">See Also</span></span>

[<span data-ttu-id="5fed8-153">encabezado SSPI. h</span><span class="sxs-lookup"><span data-stu-id="5fed8-153">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="5fed8-154">Funciones SSPI</span><span class="sxs-lookup"><span data-stu-id="5fed8-154">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="5fed8-155">Estructuras SSPI</span><span class="sxs-lookup"><span data-stu-id="5fed8-155">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


