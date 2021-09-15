---
title: Control asincrónico de canalización del lado servidor
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b0f11372090f1fd181c0d7272aa1446e5e3d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473528"
---
# <a name="server-side-asynchronous-pipe-handling"></a>Control asincrónico de canalización del lado servidor

La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor usa este identificador para enviar la respuesta y enviar los datos de canalización a medida que están disponibles. El identificador sigue siendo válido hasta que se llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) en él, [**rpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)anula la llamada o se produce una excepción en la rutina de administrador. La aplicación debe realizar un seguimiento de todos los punteros de nivel superior para los parámetros out y in, para poder actualizarlos antes de \[  \] completar la \[  \] llamada. La aplicación también debe realizar un seguimiento de las \[ [](/windows/desktop/Midl/in) \] canalizaciones de \[ [](/windows/desktop/Midl/out-idl) \] entrada y salida.

El servidor envía datos de canalización asincrónica de la misma manera que el cliente. Vea [Control de canalización asincrónica del lado cliente.](client-side-asynchronous-pipe-handling.md)

El servidor recibe datos de canalización asincrónica de la misma manera que el cliente. Si el mecanismo de recepción es llamadas a procedimiento asincrónico (APC), el servidor debe especificar un identificador de subproceso (en pAsync->u.APC.hThread) y registrar el identificador asincrónico con la biblioteca en tiempo de ejecución.

## <a name="example"></a>Ejemplo

En este ejemplo, la rutina del administrador del servidor, MyAsyncPipeFunc, controla la llamada a procedimiento remoto desde el cliente.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Pipes](pipes.md) (Operaciones de canalización de .NET Framework)
</dt> <dt>

[MIDL asincrónico](/windows/desktop/Midl/async)
</dt> <dt>

[RPC asincrónica del lado servidor](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 