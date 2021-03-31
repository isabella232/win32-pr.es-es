---
title: Control de canalizaciones asincrónicas en el servidor
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077861"
---
# <a name="server-side-asynchronous-pipe-handling"></a><span data-ttu-id="2699a-103">Control de canalizaciones asincrónicas en el servidor</span><span class="sxs-lookup"><span data-stu-id="2699a-103">Server-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="2699a-104">La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="2699a-104">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="2699a-105">El servidor usa este identificador para enviar la respuesta y enviar los datos de la canalización de salida a medida que estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="2699a-105">The server uses this handle to send the reply and to send the out pipe data as it becomes available.</span></span> <span data-ttu-id="2699a-106">El identificador sigue siendo válido hasta que se llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) en él, se anula la llamada de [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)o se produce una excepción en la rutina Manager.</span><span class="sxs-lookup"><span data-stu-id="2699a-106">The handle remains valid until [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) is called on it, the call is aborted by [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall), or an exception occurs in the manager routine.</span></span> <span data-ttu-id="2699a-107">La aplicación debe realizar un seguimiento de todos los punteros de nivel superior de los \[ parámetros **out** \] y \[ **in, out** \] , para actualizarlos antes de completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="2699a-107">The application must keep track of all top-level pointers for the \[**out**\] and \[**in, out**\] parameters, in order to update them before completing the call.</span></span> <span data-ttu-id="2699a-108">La aplicación también debe realizar un seguimiento de las \[ [](/windows/desktop/Midl/in) \] canalizaciones de salida y de \[ [**salida**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="2699a-108">The application must also keep track of the \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] pipes.</span></span>

<span data-ttu-id="2699a-109">El servidor envía datos de canalización asincrónica de la misma manera que el cliente.</span><span class="sxs-lookup"><span data-stu-id="2699a-109">The server sends asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="2699a-110">Consulte [control de canalizaciones asincrónicas en el lado cliente](client-side-asynchronous-pipe-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2699a-110">See [Client-Side Asynchronous Pipe Handling](client-side-asynchronous-pipe-handling.md).</span></span>

<span data-ttu-id="2699a-111">El servidor recibe datos de canalización asíncronos de la misma manera que el cliente.</span><span class="sxs-lookup"><span data-stu-id="2699a-111">The server receives asynchronous pipe data in the same manner as the client.</span></span> <span data-ttu-id="2699a-112">Si el mecanismo de recepción es llamadas a procedimiento asincrónico (APC), el servidor debe especificar un identificador de subproceso (en pasync->u. APC. hThread) y registrar el identificador asincrónico con la biblioteca en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2699a-112">If the receive mechanism is asynchronous procedure calls (APCs), the server must specify a thread handle (in pAsync->u.APC.hThread) and register the asynchronous handle with the run-time library.</span></span>

## <a name="example"></a><span data-ttu-id="2699a-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2699a-113">Example</span></span>

<span data-ttu-id="2699a-114">En este ejemplo, la rutina del administrador del servidor, MyAsyncPipeFunc, controla la llamada a procedimiento remoto desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="2699a-114">In this example, the server manager routine, MyAsyncPipeFunc, handles the remote procedure call from the client.</span></span>


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2699a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2699a-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2699a-116">[Pipes](pipes.md) (Operaciones de canalización de .NET Framework)</span><span class="sxs-lookup"><span data-stu-id="2699a-116">[Pipes](pipes.md)</span></span>
</dt> <dt>

[<span data-ttu-id="2699a-117">MIDL asincrónico</span><span class="sxs-lookup"><span data-stu-id="2699a-117">Asynchronous MIDL</span></span>](/windows/desktop/Midl/async)
</dt> <dt>

[<span data-ttu-id="2699a-118">RPC asincrónica del lado servidor</span><span class="sxs-lookup"><span data-stu-id="2699a-118">Server-Side Asynchronous RPC</span></span>](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 