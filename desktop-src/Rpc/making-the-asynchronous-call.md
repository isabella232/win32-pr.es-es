---
title: Realización de la llamada asincrónica
description: Antes de que pueda realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico. Los programas de cliente y servidor usan punteros a \_ la \_ estructura de estado de RPC Async para los identificadores asincrónicos.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- RPC llamada a procedimiento remoto, tareas, realizar llamadas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676439"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="cd648-105">Realización de la llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="cd648-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="cd648-106">Antes de que pueda realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico.</span><span class="sxs-lookup"><span data-stu-id="cd648-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="cd648-107">Los programas de cliente y servidor usan punteros a la estructura de [**\_ \_ Estado de RPC Async**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para los identificadores asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="cd648-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="cd648-108">Cada llamada pendiente debe tener su propio identificador asincrónico único.</span><span class="sxs-lookup"><span data-stu-id="cd648-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="cd648-109">El cliente crea el identificador y lo pasa a la función [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="cd648-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="cd648-110">Para que la llamada se complete correctamente, el cliente debe asegurarse de que la memoria para el identificador no se libere hasta que reciba la respuesta asincrónica del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd648-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="cd648-111">Además, antes de realizar otra llamada en un identificador asincrónico existente, el cliente debe reinicializar el identificador.</span><span class="sxs-lookup"><span data-stu-id="cd648-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="cd648-112">Si no lo hace, el código auxiliar del cliente puede provocar una excepción durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="cd648-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="cd648-113">El cliente también debe asegurarse de que los búferes que proporciona para los \[ parámetros [**out**](/windows/desktop/Midl/out-idl) \] y \[ [**en**](/windows/desktop/Midl/in), los parámetros **out** de \] un procedimiento remoto asincrónico permanecen asignados hasta que se ha recibido la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd648-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="cd648-114">Cuando invoca un procedimiento remoto asincrónico, el cliente debe seleccionar el método que la biblioteca en tiempo de ejecución de RPC utilizará para notificar la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cd648-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="cd648-115">El cliente puede recibir esta notificación de cualquiera de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="cd648-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="cd648-116">Ceso.</span><span class="sxs-lookup"><span data-stu-id="cd648-116">Event.</span></span> <span data-ttu-id="cd648-117">El cliente puede especificar un evento que se va a desencadenar cuando se complete la llamada.</span><span class="sxs-lookup"><span data-stu-id="cd648-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="cd648-118">Para obtener más información, consulte [objetos de evento](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="cd648-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="cd648-119">Sondeo.</span><span class="sxs-lookup"><span data-stu-id="cd648-119">Polling.</span></span> <span data-ttu-id="cd648-120">El cliente puede llamar repetidamente a [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="cd648-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="cd648-121">Si el valor devuelto es distinto de RPC \_ S \_ Async \_ Call \_ Pending, se completa la llamada.</span><span class="sxs-lookup"><span data-stu-id="cd648-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="cd648-122">Este método usa más tiempo de CPU que los otros métodos descritos aquí.</span><span class="sxs-lookup"><span data-stu-id="cd648-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="cd648-123">APC.</span><span class="sxs-lookup"><span data-stu-id="cd648-123">APC.</span></span> <span data-ttu-id="cd648-124">El cliente puede especificar una [llamada a procedimiento asincrónico (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) que recibe una llamada cuando se completa la llamada.</span><span class="sxs-lookup"><span data-stu-id="cd648-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="cd648-125">Para el prototipo de la función de APC, vea [**RPCNOTIFICATION ( \_ rutina**](/previous-versions/aa375808(v=vs.80))).</span><span class="sxs-lookup"><span data-stu-id="cd648-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="cd648-126">Se llama al APC con su parámetro de evento establecido en RpcCallComplete.</span><span class="sxs-lookup"><span data-stu-id="cd648-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="cd648-127">Para que APC se envíe, el subproceso del cliente debe estar en un estado de espera de alerta.</span><span class="sxs-lookup"><span data-stu-id="cd648-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="cd648-128">Si el campo **hThread** del identificador asincrónico se establece en 0, el APC se pone en cola en el subproceso que realizó la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd648-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="cd648-129">Si es distinto de cero, los APC se ponen en cola en el subproceso especificado por m.</span><span class="sxs-lookup"><span data-stu-id="cd648-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="cd648-130">IOC.</span><span class="sxs-lookup"><span data-stu-id="cd648-130">IOC.</span></span> <span data-ttu-id="cd648-131">El puerto de finalización de e/s recibe una notificación con los parámetros especificados en el identificador asincrónico.</span><span class="sxs-lookup"><span data-stu-id="cd648-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="cd648-132">Para obtener más información, vea [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span><span class="sxs-lookup"><span data-stu-id="cd648-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="cd648-133">Identificador de Windows.</span><span class="sxs-lookup"><span data-stu-id="cd648-133">Windows handle.</span></span> <span data-ttu-id="cd648-134">Se envía un mensaje al identificador de ventana especificado (HWND).</span><span class="sxs-lookup"><span data-stu-id="cd648-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="cd648-135">En el fragmento de código siguiente se muestran los pasos esenciales necesarios para inicializar un identificador asincrónico y usarlo para realizar una llamada asincrónica a un procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="cd648-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="cd648-136">Como se muestra en este ejemplo, el programa cliente puede ejecutar llamadas a procedimiento remoto sincrónicas mientras una llamada a un procedimiento asincrónico todavía está pendiente.</span><span class="sxs-lookup"><span data-stu-id="cd648-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="cd648-137">Este cliente crea un objeto de evento para que la biblioteca en tiempo de ejecución de RPC lo use para recibir una notificación cuando se complete la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd648-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="cd648-138">La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se genera una excepción RPC durante una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd648-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 