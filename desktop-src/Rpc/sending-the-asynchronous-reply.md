---
title: Envío de la respuesta asincrónica
description: Una vez completada la llamada asincrónica, el servidor envía una respuesta al cliente llamando a la función RpcAsyncCompleteCall y pasando el identificador asincrónico.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473544"
---
# <a name="sending-the-asynchronous-reply"></a>Envío de la respuesta asincrónica

Una vez completada la llamada asincrónica, el servidor envía una respuesta al cliente llamando a la [**función RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y pasando el identificador asincrónico. Esta llamada es necesaria incluso si la llamada asincrónica tiene un valor devuelto void y ningún \[ parámetro \] out. Si la función tiene un valor devuelto, se pasa por referencia a **RpcAsyncCompleteCall.**

Cuando el servidor llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) o **RpcAsyncAbortCall,** o se completa una llamada porque se ha generado una excepción en la rutina del administrador del servidor, la biblioteca en tiempo de ejecución rpc destruye automáticamente el identificador asincrónico del servidor.

> [!Note]  
> El servidor debe terminar de actualizar los \[ parámetros de entrada, salida \] y salida antes de llamar a \[ \] **RpcAsyncCompleteCall.** No se puede realizar ningún cambio en esos parámetros o en el identificador asincrónico después de llamar a **RpcAsyncCompleteCall.** Si se produce un error en la llamada a la función **RpcAsyncCompleteCall,** el tiempo de ejecución de RPC libera los parámetros.

 

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



Por motivos de simplicidad, esta rutina asincrónica de servidor no procesa los datos reales. Simplemente se pone a modo de suspensión durante un tiempo.

> [!Note]  
> Se puede llamar a la función **RpcAsyncCompleteCall** en el subproceso que recibió la llamada o en cualquier otro subproceso del proceso. Si todos los datos necesarios para completar la llamada están disponibles fácilmente, el servidor puede rellenarlos en el mismo subproceso y llamar a **RpcAsyncCompleteCall** en el mismo subproceso. Este enfoque ahorra cierto cambio de contexto y mejora el rendimiento. Estas llamadas se denominan asincrónicas oportunistamente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ESTADO \_ ASINCRÓNICO RPC \_**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




