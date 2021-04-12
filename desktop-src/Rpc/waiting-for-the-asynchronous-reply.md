---
title: Esperando la respuesta asincrónica
description: Lo que hace el cliente mientras espera recibir una respuesta del servidor depende del mecanismo de notificación que seleccione.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- RPC llamada a procedimiento remoto, tareas, esperar respuestas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359224"
---
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="cf7c2-104">Esperando la respuesta asincrónica</span><span class="sxs-lookup"><span data-stu-id="cf7c2-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="cf7c2-105">Lo que hace el cliente mientras espera recibir una respuesta del servidor depende del mecanismo de notificación que seleccione.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="cf7c2-106">Si el cliente usa un evento para la notificación, normalmente llamará a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o a la función [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) .</span><span class="sxs-lookup"><span data-stu-id="cf7c2-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="cf7c2-107">El cliente entra en un estado bloqueado cuando llama a cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="cf7c2-108">Esto es eficaz porque el cliente no consume ciclos de ejecución de la CPU mientras está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="cf7c2-109">Cuando usa el sondeo para esperar los resultados, el programa cliente entra en un bucle que llama repetidamente a la función [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="cf7c2-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="cf7c2-110">Se trata de un método eficaz de espera si el programa cliente realiza otro procesamiento en el bucle de sondeo.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="cf7c2-111">Por ejemplo, puede preparar los datos en fragmentos pequeños para una llamada a procedimiento remoto asincrónica subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="cf7c2-112">Una vez finalizado cada fragmento, el cliente puede sondear la llamada a procedimiento remoto asincrónica pendiente para ver si se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="cf7c2-113">El programa cliente puede proporcionar una llamada a procedimiento asincrónico (APC), que es un tipo de función de devolución de llamada que la biblioteca en tiempo de ejecución de RPC invocará cuando se complete la llamada a procedimiento remoto asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="cf7c2-114">El programa cliente debe estar en un estado de espera de alerta.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="cf7c2-115">Normalmente, esto significa que el cliente llama a una función de la API de Windows para que se ponga en estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="cf7c2-116">Para obtener más información, vea [llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="cf7c2-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="cf7c2-117">La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se genera una excepción RPC durante una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="cf7c2-118">Si el programa cliente usa un puerto de finalización de e/s para recibir la notificación de finalización, debe llamar a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="cf7c2-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="cf7c2-119">Cuando lo hace, puede esperar indefinidamente una respuesta o seguir realizando otro procesamiento.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="cf7c2-120">Si realiza otro procesamiento mientras espera una respuesta, debe sondear el puerto de finalización con la función **GetQueuedCompletionStatus** .</span><span class="sxs-lookup"><span data-stu-id="cf7c2-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="cf7c2-121">En este caso, normalmente es necesario establecer *dwMilliseconds* en cero.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="cf7c2-122">Esto hace que **GetQueuedCompletionStatus** se devuelva inmediatamente, aunque no se haya completado la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="cf7c2-123">Los programas cliente también pueden recibir notificaciones de finalización a través de sus colas de mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="cf7c2-124">En esta situación, simplemente procesan el mensaje de finalización como cualquier mensaje de Windows.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="cf7c2-125">En una aplicación multiproceso, el cliente solo puede cancelar una llamada asincrónica una vez que el subproceso que originó la llamada se ha devuelto correctamente desde la llamada.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="cf7c2-126">Esto garantiza que otro subproceso no cancele la llamada de forma asincrónica después de que se haya producido un error en una llamada sincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="cf7c2-127">Como práctica estándar, una llamada asincrónica que genera un error sincrónicamente no se debe cancelar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="cf7c2-128">La aplicación cliente debe observar este comportamiento si se pueden emitir y cancelar llamadas en subprocesos diferentes.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="cf7c2-129">Además, después de que se cancele la llamada, el código de cliente debe esperar la notificación de finalización y completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="cf7c2-130">La función [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) simplemente realiza una prisa en la notificación de finalización. no es un sustituto de la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="cf7c2-131">En el fragmento de código siguiente se muestra cómo un programa cliente puede usar un evento para esperar una respuesta asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="cf7c2-132">Los programas cliente que usan una APC para recibir la notificación de una respuesta asincrónica normalmente se ponen en estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="cf7c2-133">En el fragmento de código siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="cf7c2-134">En este caso, el programa cliente entra en suspensión y no está consumiendo ningún ciclo de CPU, hasta que la biblioteca en tiempo de ejecución de RPC llama a APC (no se muestra).</span><span class="sxs-lookup"><span data-stu-id="cf7c2-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="cf7c2-135">En el ejemplo siguiente se muestra un cliente que utiliza un puerto de finalización de e/s para esperar una respuesta asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="cf7c2-136">En el ejemplo anterior, la llamada a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) espera indefinidamente hasta que se completa la llamada a procedimiento remoto asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="cf7c2-137">Al escribir aplicaciones multiproceso, se produce una posible dificultad.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="cf7c2-138">Si un subproceso invoca una llamada a procedimiento remoto y, a continuación, finaliza antes de recibir la notificación de que se ha completado el envío, la llamada a procedimiento remoto puede producir un error y el código auxiliar del cliente puede cerrar la conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="cf7c2-139">Por lo tanto, los subprocesos que llaman a un procedimiento remoto no deben finalizar antes de que la llamada se complete o se cancele cuando no se desea el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="cf7c2-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 