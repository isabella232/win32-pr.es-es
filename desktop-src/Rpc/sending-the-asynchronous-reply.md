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
# <a name="sending-the-asynchronous-reply"></a>Enviar la respuesta asincrónica

Cuando se completa la llamada asincrónica, el servidor envía una respuesta al cliente mediante una llamada a la función [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y pasándole el identificador asincrónico. Esta llamada es necesaria incluso si la llamada asincrónica tiene un valor de devolución de void y no hay \[ parámetros de salida \] . Si la función tiene un valor devuelto, se pasa por referencia a **RpcAsyncCompleteCall**.

Cuando el servidor llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) o **RpcAsyncAbortCall**, o cuando se completa una llamada porque se produjo una excepción en la rutina del administrador de servidores, la biblioteca en tiempo de ejecución de RPC destruye automáticamente el identificador asincrónico del servidor.

> [!Note]  
> El servidor debe terminar de actualizar los \[ parámetros in, out \] y \[ out \] antes de llamar a **RpcAsyncCompleteCall**. No se pueden realizar cambios en esos parámetros o en el identificador asincrónico después de llamar a **RpcAsyncCompleteCall**. Si se produce un error en la llamada a la función **RpcAsyncCompleteCall** , el tiempo de ejecución de RPC libera los parámetros.

 

En el ejemplo siguiente se muestra una llamada a procedimiento asincrónico simple.


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



Por simplicidad, esta rutina de servidor asincrónica no procesa los datos reales. Simplemente se pone en suspensión durante un rato.

> [!Note]  
> Se puede llamar a la función **RpcAsyncCompleteCall** en el subproceso que recibió la llamada o en cualquier otro subproceso del proceso. Si todos los datos necesarios para completar la llamada están disponibles fácilmente, el servidor puede rellenarlos en el mismo subproceso y llamar a **RpcAsyncCompleteCall** en el mismo subproceso. Este enfoque guarda algún cambio de contexto y mejora el rendimiento. Dichas llamadas se denominan asincrónicamente asincrónicas.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Estado de RPC \_ Async \_**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




