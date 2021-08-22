---
title: Realizar la llamada asincrónica
description: Para poder realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico. Los programas de cliente y servidor usan punteros a la estructura RPC \_ ASYNC \_ STATE para los identificadores asincrónicos.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Llamada a procedimiento remoto RPC, tareas, realización de llamadas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928381"
---
# <a name="making-the-asynchronous-call"></a>Realizar la llamada asincrónica

Para poder realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico. Los programas de cliente y servidor usan punteros a la [**estructura RPC \_ ASYNC \_ STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para los identificadores asincrónicos.

Cada llamada pendiente debe tener su propio identificador asincrónico único. El cliente crea el identificador y lo pasa a la [**función RpcAsyncInitializeHandle.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) Para que la llamada se complete correctamente, el cliente debe asegurarse de que la memoria del identificador no se libera hasta que recibe la respuesta asincrónica del servidor. Además, antes de realizar otra llamada en un identificador asincrónico existente, el cliente debe reinicializar el identificador. Si no lo hace, el código auxiliar del cliente puede generar una excepción durante la llamada. El cliente también debe asegurarse de que los búferes que proporciona para los parámetros out y en , los parámetros out para un procedimiento remoto asincrónico permanecen asignados hasta que ha recibido la respuesta \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in)  \] del servidor.

Cuando invoca un procedimiento remoto asincrónico, el cliente debe seleccionar el método que usará la biblioteca en tiempo de ejecución rpc para notificarle la finalización de la llamada. El cliente puede recibir esta notificación de cualquiera de las maneras siguientes:

-   Evento. El cliente puede especificar un evento que se va a desencadenar cuando se haya completado la llamada. Para obtener más información, vea [Objetos de evento](/windows/desktop/Sync/event-objects).
-   Sondeo. El cliente puede llamar repetidamente a [**RpcAsyncGetCallStatus.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus) Si el valor devuelto es distinto de RPC \_ S \_ ASYNC \_ CALL \_ PENDING, la llamada se completa. Este método usa más tiempo de CPU que los demás métodos descritos aquí.
-   Apc. El cliente puede especificar una [llamada a procedimiento asincrónico (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) a la que se llama cuando se completa la llamada. Para obtener el prototipo de la función APC, vea [**RPCNOTIFICATION \_ ROUTINE**](/previous-versions/aa375808(v=vs.80)). Se llama al APC con su parámetro Event establecido en RpcCallComplete. Para que las API se envíen, el subproceso de cliente debe estar en un estado de espera que pueda recibir alertas.

    Si el **campo hThread** del identificador asincrónico se establece en 0, las API se ponen en cola en el subproceso que realizó la llamada asincrónica. Si es distinto de cero, las API se ponen en cola en el subproceso especificado por m.

-   Ioc. El puerto de finalización de E/S se notifica con los parámetros especificados en el identificador asincrónico. Para obtener más información, [**vea CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Windows identificador. Se publica un mensaje en el identificador de ventana especificado (HWND).

En el fragmento de código siguiente se muestran los pasos esenciales necesarios para inicializar un identificador asincrónico y usarlo para realizar una llamada a procedimiento remoto asincrónico.


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



Como se muestra en este ejemplo, el programa cliente puede ejecutar llamadas a procedimiento remoto sincrónico mientras una llamada a procedimiento asincrónico todavía está pendiente. Este cliente crea un objeto de evento para que la biblioteca en tiempo de ejecución rpc la use para notificarle cuando se complete la llamada asincrónica.

> [!Note]  
> La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se produce una excepción RPC durante una llamada asincrónica.

 

 

 