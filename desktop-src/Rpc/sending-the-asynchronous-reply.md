---
title: Enviar la respuesta asincrónica
description: Cuando se completa la llamada asincrónica, el servidor envía una respuesta al cliente mediante una llamada a la función RpcAsyncCompleteCall y pasándole el identificador asincrónico.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076173"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="75aff-103">Enviar la respuesta asincrónica</span><span class="sxs-lookup"><span data-stu-id="75aff-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="75aff-104">Cuando se completa la llamada asincrónica, el servidor envía una respuesta al cliente mediante una llamada a la función [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y pasándole el identificador asincrónico.</span><span class="sxs-lookup"><span data-stu-id="75aff-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="75aff-105">Esta llamada es necesaria incluso si la llamada asincrónica tiene un valor de devolución de void y no hay \[ parámetros de salida \] .</span><span class="sxs-lookup"><span data-stu-id="75aff-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="75aff-106">Si la función tiene un valor devuelto, se pasa por referencia a **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="75aff-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="75aff-107">Cuando el servidor llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) o **RpcAsyncAbortCall**, o cuando se completa una llamada porque se produjo una excepción en la rutina del administrador de servidores, la biblioteca en tiempo de ejecución de RPC destruye automáticamente el identificador asincrónico del servidor.</span><span class="sxs-lookup"><span data-stu-id="75aff-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="75aff-108">El servidor debe terminar de actualizar los \[ parámetros in, out \] y \[ out \] antes de llamar a **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="75aff-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="75aff-109">No se pueden realizar cambios en esos parámetros o en el identificador asincrónico después de llamar a **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="75aff-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="75aff-110">Si se produce un error en la llamada a la función **RpcAsyncCompleteCall** , el tiempo de ejecución de RPC libera los parámetros.</span><span class="sxs-lookup"><span data-stu-id="75aff-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="75aff-111">En el ejemplo siguiente se muestra una llamada a procedimiento asincrónico simple.</span><span class="sxs-lookup"><span data-stu-id="75aff-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



<span data-ttu-id="75aff-112">Por simplicidad, esta rutina de servidor asincrónica no procesa los datos reales.</span><span class="sxs-lookup"><span data-stu-id="75aff-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="75aff-113">Simplemente se pone en suspensión durante un rato.</span><span class="sxs-lookup"><span data-stu-id="75aff-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="75aff-114">Se puede llamar a la función **RpcAsyncCompleteCall** en el subproceso que recibió la llamada o en cualquier otro subproceso del proceso.</span><span class="sxs-lookup"><span data-stu-id="75aff-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="75aff-115">Si todos los datos necesarios para completar la llamada están disponibles fácilmente, el servidor puede rellenarlos en el mismo subproceso y llamar a **RpcAsyncCompleteCall** en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="75aff-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="75aff-116">Este enfoque guarda algún cambio de contexto y mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="75aff-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="75aff-117">Dichas llamadas se denominan asincrónicamente asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="75aff-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75aff-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75aff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75aff-119">**Estado de RPC \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="75aff-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="75aff-120">**RpcAsyncCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="75aff-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="75aff-121">**RpcAsyncAbortCall**</span><span class="sxs-lookup"><span data-stu-id="75aff-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="75aff-122">**RpcServerTestCancel**</span><span class="sxs-lookup"><span data-stu-id="75aff-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




